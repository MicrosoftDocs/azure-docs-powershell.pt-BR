---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610192"
---
# <span data-ttu-id="314ae-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="314ae-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="314ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="314ae-102">SYNOPSIS</span></span>
<span data-ttu-id="314ae-103">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="314ae-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="314ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="314ae-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="314ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="314ae-105">DESCRIPTION</span></span>
<span data-ttu-id="314ae-106">O cmdlet **set-AzureRmRecoveryServicesVaultContext** define o contexto do cofre dos serviços do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="314ae-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="314ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="314ae-107">EXAMPLES</span></span>

## <span data-ttu-id="314ae-108">OS</span><span class="sxs-lookup"><span data-stu-id="314ae-108">PARAMETERS</span></span>

### <span data-ttu-id="314ae-109">-Cofre</span><span class="sxs-lookup"><span data-stu-id="314ae-109">-Vault</span></span>
<span data-ttu-id="314ae-110">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="314ae-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="314ae-111">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="314ae-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="314ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314ae-112">-DefaultProfile</span></span>
<span data-ttu-id="314ae-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="314ae-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="314ae-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314ae-114">CommonParameters</span></span>
<span data-ttu-id="314ae-115">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314ae-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314ae-116">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314ae-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314ae-117">SENSORES</span><span class="sxs-lookup"><span data-stu-id="314ae-117">INPUTS</span></span>

### <span data-ttu-id="314ae-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="314ae-118">ARSVault</span></span>
<span data-ttu-id="314ae-119">O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="314ae-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="314ae-120">EXIBE</span><span class="sxs-lookup"><span data-stu-id="314ae-120">OUTPUTS</span></span>

## <span data-ttu-id="314ae-121">INFORMA</span><span class="sxs-lookup"><span data-stu-id="314ae-121">NOTES</span></span>

## <span data-ttu-id="314ae-122">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="314ae-122">RELATED LINKS</span></span>

