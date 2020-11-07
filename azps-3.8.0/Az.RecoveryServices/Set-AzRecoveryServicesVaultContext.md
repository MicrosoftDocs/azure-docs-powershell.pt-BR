---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943523"
---
# <span data-ttu-id="37cd6-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="37cd6-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="37cd6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37cd6-102">SYNOPSIS</span></span>

<span data-ttu-id="37cd6-103">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="37cd6-103">Sets vault context.</span></span>

## <span data-ttu-id="37cd6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37cd6-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37cd6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37cd6-105">DESCRIPTION</span></span>

<span data-ttu-id="37cd6-106">O cmdlet **set-AzRecoveryServicesVaultContext** define o contexto do cofre dos serviços do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="37cd6-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="37cd6-107">Aviso: Este cmdlet está sendo preterido em uma versão futura de alterações significativas.</span><span class="sxs-lookup"><span data-stu-id="37cd6-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="37cd6-108">Não haverá substituição para isso.</span><span class="sxs-lookup"><span data-stu-id="37cd6-108">There will be no replacement for it.</span></span> <span data-ttu-id="37cd6-109">Use o parâmetro-Cofreid em todos os comandos dos serviços de recuperação que serão encaminhados.</span><span class="sxs-lookup"><span data-stu-id="37cd6-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="37cd6-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37cd6-110">EXAMPLES</span></span>

### <span data-ttu-id="37cd6-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37cd6-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="37cd6-112">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="37cd6-112">Sets vault context.</span></span>

## <span data-ttu-id="37cd6-113">OS</span><span class="sxs-lookup"><span data-stu-id="37cd6-113">PARAMETERS</span></span>

### <span data-ttu-id="37cd6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cd6-114">-DefaultProfile</span></span>

<span data-ttu-id="37cd6-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37cd6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37cd6-116">-Cofre</span><span class="sxs-lookup"><span data-stu-id="37cd6-116">-Vault</span></span>

<span data-ttu-id="37cd6-117">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="37cd6-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="37cd6-118">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="37cd6-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="37cd6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cd6-119">CommonParameters</span></span>
<span data-ttu-id="37cd6-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37cd6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cd6-121">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37cd6-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cd6-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37cd6-122">INPUTS</span></span>

### <span data-ttu-id="37cd6-123">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="37cd6-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="37cd6-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37cd6-124">OUTPUTS</span></span>

### <span data-ttu-id="37cd6-125">System. void</span><span class="sxs-lookup"><span data-stu-id="37cd6-125">System.Void</span></span>

## <span data-ttu-id="37cd6-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37cd6-126">NOTES</span></span>

## <span data-ttu-id="37cd6-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37cd6-127">RELATED LINKS</span></span>
