---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: d1c52cef6548f8762f972789a1fd9d47e8cc92aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610328"
---
# <span data-ttu-id="83eae-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="83eae-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="83eae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="83eae-102">SYNOPSIS</span></span>
<span data-ttu-id="83eae-103">Obtém todas as SKUs válidas às quais esta IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="83eae-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83eae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83eae-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83eae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="83eae-105">DESCRIPTION</span></span>
<span data-ttu-id="83eae-106">Obtém todos os SKUs válidos para os quais esta IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="83eae-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="83eae-107">Um IotHub não pode passar entre SKUs gratuitos e pagos e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="83eae-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="83eae-108">Você terá que excluir e recriar a iothub, se quiser conseguir isso.</span><span class="sxs-lookup"><span data-stu-id="83eae-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="83eae-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="83eae-109">EXAMPLES</span></span>

### <span data-ttu-id="83eae-110">Exemplo 1 obter os SKUs válidos</span><span class="sxs-lookup"><span data-stu-id="83eae-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="83eae-111">Obtém uma lista de todos os SKUs para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="83eae-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="83eae-112">OS</span><span class="sxs-lookup"><span data-stu-id="83eae-112">PARAMETERS</span></span>

### <span data-ttu-id="83eae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83eae-113">-DefaultProfile</span></span>
<span data-ttu-id="83eae-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="83eae-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83eae-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="83eae-115">-Name</span></span>
<span data-ttu-id="83eae-116">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="83eae-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83eae-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83eae-117">-ResourceGroupName</span></span>
<span data-ttu-id="83eae-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="83eae-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83eae-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83eae-119">CommonParameters</span></span>
<span data-ttu-id="83eae-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83eae-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83eae-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83eae-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83eae-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="83eae-122">INPUTS</span></span>

### <span data-ttu-id="83eae-123">System. String</span><span class="sxs-lookup"><span data-stu-id="83eae-123">System.String</span></span>

## <span data-ttu-id="83eae-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="83eae-124">OUTPUTS</span></span>

### <span data-ttu-id="83eae-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="83eae-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="83eae-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="83eae-126">NOTES</span></span>

## <span data-ttu-id="83eae-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="83eae-127">RELATED LINKS</span></span>
