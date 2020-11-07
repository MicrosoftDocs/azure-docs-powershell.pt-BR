---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f2d7c10e29209870d4aa6e5176731b07f7695aff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776702"
---
# <span data-ttu-id="ff297-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="ff297-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="ff297-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ff297-102">SYNOPSIS</span></span>
<span data-ttu-id="ff297-103">Obtém todas as SKUs válidas às quais esta IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="ff297-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="ff297-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ff297-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ff297-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ff297-105">DESCRIPTION</span></span>
<span data-ttu-id="ff297-106">Obtém todos os SKUs válidos para os quais esta IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="ff297-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="ff297-107">Um IotHub não pode passar entre SKUs gratuitos e pagos e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="ff297-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="ff297-108">Você terá que excluir e recriar a iothub, se quiser conseguir isso.</span><span class="sxs-lookup"><span data-stu-id="ff297-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="ff297-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ff297-109">EXAMPLES</span></span>

### <span data-ttu-id="ff297-110">Exemplo 1 obter os SKUs válidos</span><span class="sxs-lookup"><span data-stu-id="ff297-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="ff297-111">Obtém uma lista de todos os SKUs para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="ff297-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="ff297-112">OS</span><span class="sxs-lookup"><span data-stu-id="ff297-112">PARAMETERS</span></span>

### <span data-ttu-id="ff297-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff297-113">-DefaultProfile</span></span>
<span data-ttu-id="ff297-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ff297-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff297-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff297-115">-Name</span></span>
<span data-ttu-id="ff297-116">Nome do Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="ff297-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="ff297-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff297-117">-ResourceGroupName</span></span>
<span data-ttu-id="ff297-118">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ff297-118">Resource Group Name</span></span>

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

### <span data-ttu-id="ff297-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff297-119">CommonParameters</span></span>
<span data-ttu-id="ff297-120">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff297-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff297-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff297-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff297-122">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ff297-122">INPUTS</span></span>

### <span data-ttu-id="ff297-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ff297-123">System.String</span></span>

## <span data-ttu-id="ff297-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ff297-124">OUTPUTS</span></span>

### <span data-ttu-id="ff297-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="ff297-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="ff297-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ff297-126">NOTES</span></span>

## <span data-ttu-id="ff297-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ff297-127">RELATED LINKS</span></span>
