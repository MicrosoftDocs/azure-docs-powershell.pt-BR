---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 8530dbff2e348f1b068afe7293cae9c993ce064e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431158"
---
# <span data-ttu-id="53f19-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="53f19-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="53f19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53f19-102">SYNOPSIS</span></span>
<span data-ttu-id="53f19-103">Exclui um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="53f19-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53f19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53f19-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53f19-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53f19-105">DESCRIPTION</span></span>
<span data-ttu-id="53f19-106">O cmdlet **Remove-AzureRmBackupVault** exclui um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="53f19-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="53f19-107">Para que você possa excluir um cofre de backup, ele deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="53f19-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="53f19-108">Use o cmdlet **Remove-AzureRmBackupContainer** para remover dados de backup da máquina virtual do IaaS (infraestrutura como serviço) do cofre.</span><span class="sxs-lookup"><span data-stu-id="53f19-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="53f19-109">Use o cmdlet **delete-RegisteredServer** para remover outros servidores registrados e dados de backup.</span><span class="sxs-lookup"><span data-stu-id="53f19-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="53f19-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53f19-110">EXAMPLES</span></span>

### <span data-ttu-id="53f19-111">Exemplo 1: excluir um cofre de backup do Azure</span><span class="sxs-lookup"><span data-stu-id="53f19-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="53f19-112">Esse comando obtém o cofre de backup do Azure chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="53f19-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="53f19-113">O comando passa o cofre para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="53f19-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53f19-114">O cmdlet atual remove o cofre.</span><span class="sxs-lookup"><span data-stu-id="53f19-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="53f19-115">OS</span><span class="sxs-lookup"><span data-stu-id="53f19-115">PARAMETERS</span></span>

### <span data-ttu-id="53f19-116">-Force</span><span class="sxs-lookup"><span data-stu-id="53f19-116">-Force</span></span>
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

### <span data-ttu-id="53f19-117">-Cofre</span><span class="sxs-lookup"><span data-stu-id="53f19-117">-Vault</span></span>
<span data-ttu-id="53f19-118">Especifica um cofre de backup que o cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="53f19-118">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="53f19-119">Para obter um **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="53f19-119">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53f19-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="53f19-120">-Confirm</span></span>
<span data-ttu-id="53f19-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53f19-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53f19-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53f19-122">-WhatIf</span></span>
<span data-ttu-id="53f19-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="53f19-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53f19-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="53f19-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53f19-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f19-125">-DefaultProfile</span></span>
<span data-ttu-id="53f19-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="53f19-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53f19-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f19-127">CommonParameters</span></span>
<span data-ttu-id="53f19-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f19-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f19-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53f19-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f19-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53f19-130">INPUTS</span></span>

### <span data-ttu-id="53f19-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="53f19-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="53f19-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53f19-132">OUTPUTS</span></span>

### <span data-ttu-id="53f19-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="53f19-133">None</span></span>

## <span data-ttu-id="53f19-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53f19-134">NOTES</span></span>
* <span data-ttu-id="53f19-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="53f19-135">None</span></span>

## <span data-ttu-id="53f19-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53f19-136">RELATED LINKS</span></span>

[<span data-ttu-id="53f19-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="53f19-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="53f19-138">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="53f19-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="53f19-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="53f19-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


