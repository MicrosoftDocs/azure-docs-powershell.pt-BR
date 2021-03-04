---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: b51c41ddd36d19afedd0091be9b0a00bb447faaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886963"
---
# <span data-ttu-id="d6180-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="d6180-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="d6180-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6180-102">SYNOPSIS</span></span>
<span data-ttu-id="d6180-103">Obtém todos os skus válidos para os que esse IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="d6180-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="d6180-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d6180-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6180-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d6180-105">DESCRIPTION</span></span>
<span data-ttu-id="d6180-106">Obtém todos os skus válidos para os que esse IotHub pode fazer a transição.</span><span class="sxs-lookup"><span data-stu-id="d6180-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="d6180-107">Um IotHub não pode fazer a transição entre os skus gratuitos e os pagos e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="d6180-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="d6180-108">Você terá que excluir e recriar o iothub se quiser fazer isso.</span><span class="sxs-lookup"><span data-stu-id="d6180-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="d6180-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6180-109">EXAMPLES</span></span>

### <span data-ttu-id="d6180-110">Exemplo 1 Obter os skus válidos</span><span class="sxs-lookup"><span data-stu-id="d6180-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d6180-111">Obtém uma lista de todos os skus para o IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="d6180-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="d6180-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d6180-112">PARAMETERS</span></span>

### <span data-ttu-id="d6180-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6180-113">-DefaultProfile</span></span>
<span data-ttu-id="d6180-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="d6180-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6180-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d6180-115">-Name</span></span>
<span data-ttu-id="d6180-116">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="d6180-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="d6180-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6180-117">-ResourceGroupName</span></span>
<span data-ttu-id="d6180-118">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="d6180-118">Resource Group Name</span></span>

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

### <span data-ttu-id="d6180-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6180-119">CommonParameters</span></span>
<span data-ttu-id="d6180-120">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6180-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6180-121">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6180-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6180-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d6180-122">INPUTS</span></span>

### <span data-ttu-id="d6180-123">System.String</span><span class="sxs-lookup"><span data-stu-id="d6180-123">System.String</span></span>

## <span data-ttu-id="d6180-124">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d6180-124">OUTPUTS</span></span>

### <span data-ttu-id="d6180-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="d6180-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="d6180-126">NOTES</span><span class="sxs-lookup"><span data-stu-id="d6180-126">NOTES</span></span>

## <span data-ttu-id="d6180-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6180-127">RELATED LINKS</span></span>
