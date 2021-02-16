---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubquotametric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubQuotaMetric.md
ms.openlocfilehash: 1f3fc05a71ec0d7c6f4926f47f6ab862af42b9e7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113133"
---
# <span data-ttu-id="b8efd-101">Get-AzIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="b8efd-101">Get-AzIotHubQuotaMetric</span></span>

## <span data-ttu-id="b8efd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b8efd-102">SYNOPSIS</span></span>
<span data-ttu-id="b8efd-103">Obtém as Métricas de Cota para um IotHub.</span><span class="sxs-lookup"><span data-stu-id="b8efd-103">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="b8efd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8efd-104">SYNTAX</span></span>

```
Get-AzIotHubQuotaMetric [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8efd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="b8efd-105">DESCRIPTION</span></span>
<span data-ttu-id="b8efd-106">Obtém as Métricas de Cota para um IotHub.</span><span class="sxs-lookup"><span data-stu-id="b8efd-106">Gets the Quota Metrics for an IotHub.</span></span>

## <span data-ttu-id="b8efd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b8efd-107">EXAMPLES</span></span>

### <span data-ttu-id="b8efd-108">Exemplo 1 Obter as Métricas de Cota</span><span class="sxs-lookup"><span data-stu-id="b8efd-108">Example 1 Get the Quota Metrics</span></span>
```
PS C:\> Get-AzIotHubQuotaMetric -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b8efd-109">Obtém as informações da Métrica de Cota do IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="b8efd-109">Gets the Quota Metric information for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="b8efd-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b8efd-110">PARAMETERS</span></span>

### <span data-ttu-id="b8efd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8efd-111">-DefaultProfile</span></span>
<span data-ttu-id="b8efd-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b8efd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8efd-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8efd-113">-Name</span></span>
<span data-ttu-id="b8efd-114">Nome do hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="b8efd-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="b8efd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8efd-115">-ResourceGroupName</span></span>
<span data-ttu-id="b8efd-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b8efd-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b8efd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8efd-117">CommonParameters</span></span>
<span data-ttu-id="b8efd-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8efd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8efd-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8efd-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8efd-120">Entradas</span><span class="sxs-lookup"><span data-stu-id="b8efd-120">INPUTS</span></span>

### <span data-ttu-id="b8efd-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b8efd-121">System.String</span></span>

## <span data-ttu-id="b8efd-122">Saídas</span><span class="sxs-lookup"><span data-stu-id="b8efd-122">OUTPUTS</span></span>

### <span data-ttu-id="b8efd-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span><span class="sxs-lookup"><span data-stu-id="b8efd-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubQuotaMetric</span></span>

## <span data-ttu-id="b8efd-124">Notas</span><span class="sxs-lookup"><span data-stu-id="b8efd-124">NOTES</span></span>

## <span data-ttu-id="b8efd-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8efd-125">RELATED LINKS</span></span>
