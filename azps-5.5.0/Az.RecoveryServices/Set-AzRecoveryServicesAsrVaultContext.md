---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114543"
---
# <span data-ttu-id="4d347-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="4d347-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="4d347-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4d347-102">SYNOPSIS</span></span>
<span data-ttu-id="4d347-103">Define o contexto do cofre dos Serviços de Recuperação a ser usado para operações subsequentes de Recuperação de Site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d347-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="4d347-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d347-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d347-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="4d347-105">DESCRIPTION</span></span>
<span data-ttu-id="4d347-106">O **cmdlet Set-AzRecoveryServicesAsrVaultContext define** o contexto do cofre de Recuperação de Site do Azure para operações posteriores.</span><span class="sxs-lookup"><span data-stu-id="4d347-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="4d347-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4d347-107">EXAMPLES</span></span>

### <span data-ttu-id="4d347-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4d347-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="4d347-109">Define o contexto do cofre para o cofre especificado dos Serviços de Recuperação para as operações subsequentes de Recuperação de Site do Azure na sessão atual do PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4d347-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="4d347-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d347-110">PARAMETERS</span></span>

### <span data-ttu-id="4d347-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d347-111">-DefaultProfile</span></span>
<span data-ttu-id="4d347-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="4d347-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d347-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="4d347-113">-Vault</span></span>
<span data-ttu-id="4d347-114">O objeto do cofre dos Serviços de Recuperação correspondente ao cofre dos Serviços de Recuperação.</span><span class="sxs-lookup"><span data-stu-id="4d347-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="4d347-115">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4d347-115">-Confirm</span></span>
<span data-ttu-id="4d347-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d347-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d347-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d347-117">-WhatIf</span></span>
<span data-ttu-id="4d347-118">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4d347-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d347-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4d347-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d347-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d347-120">CommonParameters</span></span>
<span data-ttu-id="4d347-121">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d347-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d347-122">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d347-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d347-123">Entradas</span><span class="sxs-lookup"><span data-stu-id="4d347-123">INPUTS</span></span>

### <span data-ttu-id="4d347-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="4d347-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="4d347-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="4d347-125">OUTPUTS</span></span>

### <span data-ttu-id="4d347-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="4d347-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="4d347-127">Notas</span><span class="sxs-lookup"><span data-stu-id="4d347-127">NOTES</span></span>

## <span data-ttu-id="4d347-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4d347-128">RELATED LINKS</span></span>
