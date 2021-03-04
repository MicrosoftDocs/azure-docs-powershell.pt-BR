---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: b3d0b292d7e680ca1d16e935c34a268cea836aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885525"
---
# <span data-ttu-id="99dcb-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="99dcb-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="99dcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="99dcb-103">Exclui um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="99dcb-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="99dcb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="99dcb-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99dcb-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="99dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="99dcb-106">O cmdlet **Remove-AzRecoveryServicesVault** exclui um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="99dcb-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="99dcb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99dcb-107">EXAMPLES</span></span>

### <span data-ttu-id="99dcb-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99dcb-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="99dcb-109">Exclui um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="99dcb-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="99dcb-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="99dcb-110">PARAMETERS</span></span>

### <span data-ttu-id="99dcb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99dcb-111">-DefaultProfile</span></span>
<span data-ttu-id="99dcb-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="99dcb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99dcb-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="99dcb-113">-Vault</span></span>
<span data-ttu-id="99dcb-114">Especifica um objeto do cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="99dcb-114">Specifies an Azure Site Recovery vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99dcb-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99dcb-115">-Confirm</span></span>
<span data-ttu-id="99dcb-116">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99dcb-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99dcb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99dcb-117">-WhatIf</span></span>
<span data-ttu-id="99dcb-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99dcb-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99dcb-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99dcb-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99dcb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99dcb-120">CommonParameters</span></span>
<span data-ttu-id="99dcb-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99dcb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99dcb-122">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99dcb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99dcb-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="99dcb-123">INPUTS</span></span>

### <span data-ttu-id="99dcb-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="99dcb-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="99dcb-125">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="99dcb-125">OUTPUTS</span></span>

### <span data-ttu-id="99dcb-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="99dcb-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="99dcb-127">NOTES</span><span class="sxs-lookup"><span data-stu-id="99dcb-127">NOTES</span></span>

## <span data-ttu-id="99dcb-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99dcb-128">RELATED LINKS</span></span>

[<span data-ttu-id="99dcb-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="99dcb-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="99dcb-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="99dcb-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="99dcb-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="99dcb-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


