---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/unregister-azurermbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 8c90137e142086d7ea7c0bcc34321b3f38a12d95
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428592"
---
# <span data-ttu-id="a65b6-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a65b6-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="a65b6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a65b6-102">SYNOPSIS</span></span>
<span data-ttu-id="a65b6-103">Cancela o registro de um contêiner de um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="a65b6-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a65b6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a65b6-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a65b6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a65b6-105">DESCRIPTION</span></span>
<span data-ttu-id="a65b6-106">O cmdlet **Unregister-AzureRmBackupContainer** cancela o registro do Windows Server ou da máquina virtual do Azure a partir de um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="a65b6-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="a65b6-107">Este cmdlet Remove referências a um contêiner do cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="a65b6-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="a65b6-108">Antes de cancelar o registro de um contêiner, você deve excluir todos os dados protegidos associados a esse contêiner.</span><span class="sxs-lookup"><span data-stu-id="a65b6-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="a65b6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a65b6-109">EXAMPLES</span></span>

### <span data-ttu-id="a65b6-110">Exemplo 1: cancelar o registro de um servidor Windows</span><span class="sxs-lookup"><span data-stu-id="a65b6-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="a65b6-111">O primeiro comando obtém o cofre chamado Vault03 usando o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="a65b6-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="a65b6-112">O comando armazena esse objeto na variável $Vault.</span><span class="sxs-lookup"><span data-stu-id="a65b6-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="a65b6-113">O segundo comando obtém um contêiner que tem o nome especificado no cofre no $Vault usando o cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="a65b6-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="a65b6-114">O comando armazena esse objeto na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="a65b6-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="a65b6-115">O comando final cancela o registro do Windows Server especificado do cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="a65b6-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="a65b6-116">Exemplo 2: cancelar o registro de um servidor Windows sem confirmação</span><span class="sxs-lookup"><span data-stu-id="a65b6-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="a65b6-117">Esse comando cancela o registro do Windows Server especificado do cofre de backup do Azure, exatamente como no primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="a65b6-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="a65b6-118">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="a65b6-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a65b6-119">Portanto, o comando não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="a65b6-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="a65b6-120">OS</span><span class="sxs-lookup"><span data-stu-id="a65b6-120">PARAMETERS</span></span>

### <span data-ttu-id="a65b6-121">-Contêiner</span><span class="sxs-lookup"><span data-stu-id="a65b6-121">-Container</span></span>
<span data-ttu-id="a65b6-122">Especifica o Windows Server ou a máquina virtual do Azure que este cmdlet cancela o registro.</span><span class="sxs-lookup"><span data-stu-id="a65b6-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="a65b6-123">Para obter um **AzureRmBackupContainer** , use o cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="a65b6-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a65b6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a65b6-124">-DefaultProfile</span></span>
<span data-ttu-id="a65b6-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a65b6-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65b6-126">-Force</span><span class="sxs-lookup"><span data-stu-id="a65b6-126">-Force</span></span>
<span data-ttu-id="a65b6-127">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a65b6-127">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="a65b6-128">Esse parâmetro é relevante somente para objetos **AzureBackupContainer** do tipo Windows.</span><span class="sxs-lookup"><span data-stu-id="a65b6-128">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65b6-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a65b6-129">-Confirm</span></span>
<span data-ttu-id="a65b6-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a65b6-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65b6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a65b6-131">-WhatIf</span></span>
<span data-ttu-id="a65b6-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a65b6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a65b6-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a65b6-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a65b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a65b6-134">CommonParameters</span></span>
<span data-ttu-id="a65b6-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a65b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a65b6-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a65b6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a65b6-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a65b6-137">INPUTS</span></span>

### <span data-ttu-id="a65b6-138">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a65b6-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer</span></span>
<span data-ttu-id="a65b6-139">Parâmetros: Container (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a65b6-139">Parameters: Container (ByValue)</span></span>

## <span data-ttu-id="a65b6-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a65b6-140">OUTPUTS</span></span>

### <span data-ttu-id="a65b6-141">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="a65b6-141">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="a65b6-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a65b6-142">NOTES</span></span>
* <span data-ttu-id="a65b6-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="a65b6-143">None</span></span>

## <span data-ttu-id="a65b6-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a65b6-144">RELATED LINKS</span></span>

[<span data-ttu-id="a65b6-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a65b6-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="a65b6-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="a65b6-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="a65b6-147">Register-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="a65b6-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


