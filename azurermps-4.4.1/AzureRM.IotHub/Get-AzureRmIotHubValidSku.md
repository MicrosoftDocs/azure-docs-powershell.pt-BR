---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: 904fb627be4460fbbca0dc6dae9a68fc0dd468ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440651"
---
# <span data-ttu-id="cdfd8-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="cdfd8-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="cdfd8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cdfd8-102">SYNOPSIS</span></span>
<span data-ttu-id="cdfd8-103">Obtém todas as SKUs válidas às quais esta IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="cdfd8-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdfd8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cdfd8-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cdfd8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cdfd8-105">DESCRIPTION</span></span>
<span data-ttu-id="cdfd8-106">Obtém todos os SKUs válidos para os quais esta IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="cdfd8-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="cdfd8-107">Um IotHub não pode passar entre SKUs gratuitos e pagos e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="cdfd8-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="cdfd8-108">Você terá que excluir e recriar a iothub, se quiser conseguir isso.</span><span class="sxs-lookup"><span data-stu-id="cdfd8-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="cdfd8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdfd8-109">EXAMPLES</span></span>

### <span data-ttu-id="cdfd8-110">Exemplo 1 obter os SKUs válidos</span><span class="sxs-lookup"><span data-stu-id="cdfd8-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="cdfd8-111">Obtém uma lista de todos os SKUs para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="cdfd8-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="cdfd8-112">OS</span><span class="sxs-lookup"><span data-stu-id="cdfd8-112">PARAMETERS</span></span>

### <span data-ttu-id="cdfd8-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdfd8-113">-Name</span></span>
<span data-ttu-id="cdfd8-114">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="cdfd8-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="cdfd8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdfd8-115">-ResourceGroupName</span></span>
<span data-ttu-id="cdfd8-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cdfd8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="cdfd8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdfd8-117">-DefaultProfile</span></span>
<span data-ttu-id="cdfd8-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdfd8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdfd8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdfd8-119">CommonParameters</span></span>
<span data-ttu-id="cdfd8-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdfd8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdfd8-121">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdfd8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdfd8-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cdfd8-122">INPUTS</span></span>

### <span data-ttu-id="cdfd8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cdfd8-123">System.String</span></span>

## <span data-ttu-id="cdfd8-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cdfd8-124">OUTPUTS</span></span>

### <span data-ttu-id="cdfd8-125">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="cdfd8-125">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="cdfd8-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cdfd8-126">NOTES</span></span>

## <span data-ttu-id="cdfd8-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdfd8-127">RELATED LINKS</span></span>

