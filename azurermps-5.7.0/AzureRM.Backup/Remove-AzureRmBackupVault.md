---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 4b8098889cbec7bd313ffb2ed70c5384a7e24ef0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432972"
---
# <span data-ttu-id="c0a70-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c0a70-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="c0a70-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c0a70-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a70-103">Exclui um cofre de backup.</span><span class="sxs-lookup"><span data-stu-id="c0a70-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0a70-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0a70-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0a70-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c0a70-105">DESCRIPTION</span></span>
<span data-ttu-id="c0a70-106">O cmdlet **Remove-AzureRmBackupVault** exclui um cofre de backup do Azure.</span><span class="sxs-lookup"><span data-stu-id="c0a70-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="c0a70-107">Para que você possa excluir um cofre de backup, ele deve estar vazio.</span><span class="sxs-lookup"><span data-stu-id="c0a70-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="c0a70-108">Use o cmdlet **Remove-AzureRmBackupContainer** para remover dados de backup da máquina virtual do IaaS (infraestrutura como serviço) do cofre.</span><span class="sxs-lookup"><span data-stu-id="c0a70-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="c0a70-109">Use o cmdlet **delete-RegisteredServer** para remover outros servidores registrados e dados de backup.</span><span class="sxs-lookup"><span data-stu-id="c0a70-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="c0a70-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c0a70-110">EXAMPLES</span></span>

### <span data-ttu-id="c0a70-111">Exemplo 1: excluir um cofre de backup do Azure</span><span class="sxs-lookup"><span data-stu-id="c0a70-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="c0a70-112">Esse comando obtém o cofre de backup do Azure chamado Vault03 usando o cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="c0a70-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="c0a70-113">O comando passa o cofre para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="c0a70-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c0a70-114">O cmdlet atual remove o cofre.</span><span class="sxs-lookup"><span data-stu-id="c0a70-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="c0a70-115">OS</span><span class="sxs-lookup"><span data-stu-id="c0a70-115">PARAMETERS</span></span>

### <span data-ttu-id="c0a70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a70-116">-DefaultProfile</span></span>
<span data-ttu-id="c0a70-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c0a70-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a70-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c0a70-118">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a70-119">-Cofre</span><span class="sxs-lookup"><span data-stu-id="c0a70-119">-Vault</span></span>
<span data-ttu-id="c0a70-120">Especifica um cofre de backup que o cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c0a70-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="c0a70-121">Para obter um **AzureRmBackupVault** , use o cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="c0a70-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0a70-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c0a70-122">-Confirm</span></span>
<span data-ttu-id="c0a70-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0a70-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a70-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0a70-124">-WhatIf</span></span>
<span data-ttu-id="c0a70-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c0a70-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0a70-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c0a70-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0a70-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a70-127">CommonParameters</span></span>
<span data-ttu-id="c0a70-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0a70-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a70-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a70-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a70-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c0a70-130">INPUTS</span></span>

### <span data-ttu-id="c0a70-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="c0a70-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="c0a70-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c0a70-132">OUTPUTS</span></span>

### <span data-ttu-id="c0a70-133">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c0a70-133">None</span></span>

## <span data-ttu-id="c0a70-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c0a70-134">NOTES</span></span>
* <span data-ttu-id="c0a70-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c0a70-135">None</span></span>

## <span data-ttu-id="c0a70-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c0a70-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0a70-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c0a70-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="c0a70-138">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c0a70-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="c0a70-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c0a70-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


