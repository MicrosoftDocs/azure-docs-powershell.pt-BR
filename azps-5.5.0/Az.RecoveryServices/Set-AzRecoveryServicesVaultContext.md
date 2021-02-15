---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114540"
---
# <span data-ttu-id="9f768-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="9f768-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="9f768-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f768-102">SYNOPSIS</span></span>

<span data-ttu-id="9f768-103">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="9f768-103">Sets vault context.</span></span>

## <span data-ttu-id="9f768-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f768-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f768-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f768-105">DESCRIPTION</span></span>

<span data-ttu-id="9f768-106">O **cmdlet Set-AzRecoveryServicesVaultContext define** o contexto do cofre para os serviços de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f768-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="9f768-107">Aviso: este cmdlet está sendo preterido em um lançamento de alteração futura.</span><span class="sxs-lookup"><span data-stu-id="9f768-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="9f768-108">Não haverá substituição para ele.</span><span class="sxs-lookup"><span data-stu-id="9f768-108">There will be no replacement for it.</span></span> <span data-ttu-id="9f768-109">Use o parâmetro -VaultId em todos os comandos dos Serviços de Recuperação no futuro.</span><span class="sxs-lookup"><span data-stu-id="9f768-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="9f768-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9f768-110">EXAMPLES</span></span>

### <span data-ttu-id="9f768-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f768-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="9f768-112">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="9f768-112">Sets vault context.</span></span>

## <span data-ttu-id="9f768-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f768-113">PARAMETERS</span></span>

### <span data-ttu-id="9f768-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f768-114">-DefaultProfile</span></span>

<span data-ttu-id="9f768-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="9f768-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f768-116">-Cofre</span><span class="sxs-lookup"><span data-stu-id="9f768-116">-Vault</span></span>

<span data-ttu-id="9f768-117">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="9f768-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="9f768-118">O cofre deve ser um **objeto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="9f768-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9f768-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f768-119">CommonParameters</span></span>
<span data-ttu-id="9f768-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f768-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f768-121">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f768-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f768-122">Entradas</span><span class="sxs-lookup"><span data-stu-id="9f768-122">INPUTS</span></span>

### <span data-ttu-id="9f768-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="9f768-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9f768-124">Saídas</span><span class="sxs-lookup"><span data-stu-id="9f768-124">OUTPUTS</span></span>

### <span data-ttu-id="9f768-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="9f768-125">System.Void</span></span>

## <span data-ttu-id="9f768-126">Notas</span><span class="sxs-lookup"><span data-stu-id="9f768-126">NOTES</span></span>

## <span data-ttu-id="9f768-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f768-127">RELATED LINKS</span></span>
