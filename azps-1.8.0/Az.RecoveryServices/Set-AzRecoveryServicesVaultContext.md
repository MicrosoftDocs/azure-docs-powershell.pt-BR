---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599604"
---
# <span data-ttu-id="22e89-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="22e89-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="22e89-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="22e89-102">SYNOPSIS</span></span>
<span data-ttu-id="22e89-103">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="22e89-103">Sets vault context.</span></span>

## <span data-ttu-id="22e89-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="22e89-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22e89-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="22e89-105">DESCRIPTION</span></span>
<span data-ttu-id="22e89-106">O cmdlet **set-AzRecoveryServicesVaultContext** define o contexto do cofre dos serviços do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="22e89-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="22e89-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="22e89-107">EXAMPLES</span></span>

### <span data-ttu-id="22e89-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="22e89-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="22e89-109">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="22e89-109">Sets vault context.</span></span>

## <span data-ttu-id="22e89-110">OS</span><span class="sxs-lookup"><span data-stu-id="22e89-110">PARAMETERS</span></span>

### <span data-ttu-id="22e89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e89-111">-DefaultProfile</span></span>
<span data-ttu-id="22e89-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="22e89-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22e89-113">-Cofre</span><span class="sxs-lookup"><span data-stu-id="22e89-113">-Vault</span></span>
<span data-ttu-id="22e89-114">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="22e89-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="22e89-115">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="22e89-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="22e89-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e89-116">CommonParameters</span></span>
<span data-ttu-id="22e89-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22e89-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e89-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22e89-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e89-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="22e89-119">INPUTS</span></span>

### <span data-ttu-id="22e89-120">Microsoft. Azure. Commands. Recoveryservices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="22e89-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="22e89-121">EXIBE</span><span class="sxs-lookup"><span data-stu-id="22e89-121">OUTPUTS</span></span>

### <span data-ttu-id="22e89-122">System. void</span><span class="sxs-lookup"><span data-stu-id="22e89-122">System.Void</span></span>

## <span data-ttu-id="22e89-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="22e89-123">NOTES</span></span>

## <span data-ttu-id="22e89-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="22e89-124">RELATED LINKS</span></span>