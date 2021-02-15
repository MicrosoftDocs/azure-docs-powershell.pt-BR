---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114931"
---
# <span data-ttu-id="1e875-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1e875-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="1e875-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e875-102">SYNOPSIS</span></span>
<span data-ttu-id="1e875-103">Exclui um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="1e875-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="1e875-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e875-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e875-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e875-105">DESCRIPTION</span></span>
<span data-ttu-id="1e875-106">O **cmdlet Remove-AzRecoveryServicesVault** exclui um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="1e875-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="1e875-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e875-107">EXAMPLES</span></span>

### <span data-ttu-id="1e875-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1e875-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="1e875-109">Exclui um cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="1e875-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="1e875-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e875-110">PARAMETERS</span></span>

### <span data-ttu-id="1e875-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e875-111">-DefaultProfile</span></span>
<span data-ttu-id="1e875-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="1e875-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e875-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="1e875-113">-Vault</span></span>
<span data-ttu-id="1e875-114">Especifica um objeto do cofre de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="1e875-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="1e875-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1e875-115">-Confirm</span></span>
<span data-ttu-id="1e875-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e875-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e875-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e875-117">-WhatIf</span></span>
<span data-ttu-id="1e875-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1e875-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e875-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e875-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e875-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e875-120">CommonParameters</span></span>
<span data-ttu-id="1e875-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e875-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e875-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e875-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e875-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="1e875-123">INPUTS</span></span>

### <span data-ttu-id="1e875-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="1e875-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="1e875-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="1e875-125">OUTPUTS</span></span>

### <span data-ttu-id="1e875-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="1e875-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="1e875-127">Notas</span><span class="sxs-lookup"><span data-stu-id="1e875-127">NOTES</span></span>

## <span data-ttu-id="1e875-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e875-128">RELATED LINKS</span></span>

[<span data-ttu-id="1e875-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1e875-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="1e875-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="1e875-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="1e875-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="1e875-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


