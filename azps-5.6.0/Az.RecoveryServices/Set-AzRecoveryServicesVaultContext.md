---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 04fa3c9a7024b8a9e1f525a4ef131ae151f25804
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891293"
---
# <span data-ttu-id="e982b-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="e982b-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="e982b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e982b-102">SYNOPSIS</span></span>

<span data-ttu-id="e982b-103">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="e982b-103">Sets vault context.</span></span>

## <span data-ttu-id="e982b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e982b-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e982b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e982b-105">DESCRIPTION</span></span>

<span data-ttu-id="e982b-106">O cmdlet **Set-AzRecoveryServicesVaultContext** define o contexto do cofre para os serviços de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="e982b-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="e982b-107">Aviso: este cmdlet está sendo preterido em uma versão futura de alteração de quebra.</span><span class="sxs-lookup"><span data-stu-id="e982b-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="e982b-108">Não haverá nenhuma substituição para ele.</span><span class="sxs-lookup"><span data-stu-id="e982b-108">There will be no replacement for it.</span></span> <span data-ttu-id="e982b-109">Use o parâmetro -VaultId em todos os comandos dos Serviços de Recuperação em frente.</span><span class="sxs-lookup"><span data-stu-id="e982b-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="e982b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e982b-110">EXAMPLES</span></span>

### <span data-ttu-id="e982b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e982b-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="e982b-112">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="e982b-112">Sets vault context.</span></span>

## <span data-ttu-id="e982b-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e982b-113">PARAMETERS</span></span>

### <span data-ttu-id="e982b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e982b-114">-DefaultProfile</span></span>

<span data-ttu-id="e982b-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="e982b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e982b-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="e982b-116">-Vault</span></span>

<span data-ttu-id="e982b-117">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="e982b-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="e982b-118">O cofre deve ser um **objeto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="e982b-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="e982b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e982b-119">CommonParameters</span></span>
<span data-ttu-id="e982b-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e982b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e982b-121">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e982b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e982b-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e982b-122">INPUTS</span></span>

### <span data-ttu-id="e982b-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="e982b-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e982b-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e982b-124">OUTPUTS</span></span>

### <span data-ttu-id="e982b-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="e982b-125">System.Void</span></span>

## <span data-ttu-id="e982b-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="e982b-126">NOTES</span></span>

## <span data-ttu-id="e982b-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e982b-127">RELATED LINKS</span></span>
