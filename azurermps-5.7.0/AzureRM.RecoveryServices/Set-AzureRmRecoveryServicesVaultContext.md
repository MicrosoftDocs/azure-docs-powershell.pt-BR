---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 9329f35377731eeb3e59e01a673129b5505abf49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603244"
---
# <span data-ttu-id="2215e-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="2215e-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="2215e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2215e-102">SYNOPSIS</span></span>
<span data-ttu-id="2215e-103">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="2215e-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2215e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2215e-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2215e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2215e-105">DESCRIPTION</span></span>
<span data-ttu-id="2215e-106">O cmdlet **set-AzureRmRecoveryServicesVaultContext** define o contexto do cofre dos serviços do Azure site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2215e-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="2215e-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2215e-107">EXAMPLES</span></span>

### <span data-ttu-id="2215e-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2215e-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="2215e-109">Define o contexto do cofre.</span><span class="sxs-lookup"><span data-stu-id="2215e-109">Sets vault context.</span></span>

## <span data-ttu-id="2215e-110">OS</span><span class="sxs-lookup"><span data-stu-id="2215e-110">PARAMETERS</span></span>

### <span data-ttu-id="2215e-111">-Cofre</span><span class="sxs-lookup"><span data-stu-id="2215e-111">-Vault</span></span>
<span data-ttu-id="2215e-112">Especifica o nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="2215e-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="2215e-113">O cofre deve ser um objeto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="2215e-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2215e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2215e-114">-DefaultProfile</span></span>
<span data-ttu-id="2215e-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2215e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2215e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2215e-116">CommonParameters</span></span>
<span data-ttu-id="2215e-117">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2215e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2215e-118">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2215e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2215e-119">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2215e-119">INPUTS</span></span>

### <span data-ttu-id="2215e-120">ARSVault</span><span class="sxs-lookup"><span data-stu-id="2215e-120">ARSVault</span></span>
<span data-ttu-id="2215e-121">O parâmetro ' cofre ' aceita o valor do tipo ' ARSVault ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="2215e-121">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="2215e-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2215e-122">OUTPUTS</span></span>

## <span data-ttu-id="2215e-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2215e-123">NOTES</span></span>

## <span data-ttu-id="2215e-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2215e-124">RELATED LINKS</span></span>

