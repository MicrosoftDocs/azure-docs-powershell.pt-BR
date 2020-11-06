---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 03285628-6BD3-4F2F-8129-E3CAE4C70EC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteConfig.md
ms.openlocfilehash: b64fe52b95fb116b08aade300f622b8ea612dcc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440601"
---
# <span data-ttu-id="9f93b-101">Remove-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9f93b-101">Remove-AzureRmRouteConfig</span></span>

## <span data-ttu-id="9f93b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9f93b-102">SYNOPSIS</span></span>
<span data-ttu-id="9f93b-103">Remove uma rota de uma tabela de rota.</span><span class="sxs-lookup"><span data-stu-id="9f93b-103">Removes a route from a route table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f93b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9f93b-104">SYNTAX</span></span>

```
Remove-AzureRmRouteConfig -Name <String> -RouteTable <PSRouteTable> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f93b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9f93b-105">DESCRIPTION</span></span>
<span data-ttu-id="9f93b-106">O cmdlet **Remove-AzureRmRouteConfig** remove uma rota de uma tabela de rota do Azure.</span><span class="sxs-lookup"><span data-stu-id="9f93b-106">The **Remove-AzureRmRouteConfig** cmdlet removes a route from an Azure route table.</span></span>

## <span data-ttu-id="9f93b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f93b-107">EXAMPLES</span></span>

### <span data-ttu-id="9f93b-108">Exemplo 1: remover uma rota</span><span class="sxs-lookup"><span data-stu-id="9f93b-108">Example 1: Remove a route</span></span>
```
PS C:\>Get-AzureRmRouteTable -ResourceGroupName "ResourceGroup11" -Name "RouteTable01" | Remove-AzureRmRouteConfig -Name "Route02" | Set-AzureRmRouteTable
Name              : RouteTable01
ResourceGroupName : ResourceGroup11
Location          : eastus
Id                : /subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Microsoft.Networ
                    k/routeTables/RouteTable01
Etag              : W/"47099b62-60ec-4bc1-b87b-fad56cb8bed1"
ProvisioningState : Succeeded
Tags              : 
Routes            : [
                      {
                        "Name": "Route07",
                        "Etag": "W/\"47099b62-60ec-4bc1-b87b-fad56cb8bed1\"",
                        "Id": "/subscriptions/xxxx-xxxx-xxxx-xxxx/resourceGroups/ResourceGroup11/providers/Micro
                    soft.Network/routeTables/RouteTable01/routes/Route07",
                        "AddressPrefix": "10.1.0.0/16",
                        "NextHopType": "VnetLocal",
                        "NextHopIpAddress": null, 
                        "ProvisioningState": "Succeeded"
                      }
                    ] 
Subnets           : []
```

<span data-ttu-id="9f93b-109">Esse comando obtém a tabela de rota chamada RouteTable01 usando o cmdlet **Get-AzureRmRouteTable** .</span><span class="sxs-lookup"><span data-stu-id="9f93b-109">This command gets the route table named RouteTable01 by using the **Get-AzureRmRouteTable** cmdlet.</span></span>
<span data-ttu-id="9f93b-110">O comando transmite essa tabela para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="9f93b-110">The command passes that table to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9f93b-111">O cmdlet atual remove a rota chamada Route02 e passa o resultado para o cmdlet **set-AzureRmRouteTable** , que atualiza a tabela para refletir suas alterações.</span><span class="sxs-lookup"><span data-stu-id="9f93b-111">The current cmdlet remove the route named Route02, and the passes the result to the **Set-AzureRmRouteTable** cmdlet, which updates the table to reflect your changes.</span></span>
<span data-ttu-id="9f93b-112">A tabela não contém mais a rota chamada Route02.</span><span class="sxs-lookup"><span data-stu-id="9f93b-112">The table no longer contains the route named Route02.</span></span>

## <span data-ttu-id="9f93b-113">OS</span><span class="sxs-lookup"><span data-stu-id="9f93b-113">PARAMETERS</span></span>

### <span data-ttu-id="9f93b-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f93b-114">-Name</span></span>
<span data-ttu-id="9f93b-115">Especifica o nome da rota que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="9f93b-115">Specifies the name of the route that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f93b-116">-RouteTable</span><span class="sxs-lookup"><span data-stu-id="9f93b-116">-RouteTable</span></span>
<span data-ttu-id="9f93b-117">Especifica a tabela de rota que contém a rota que este cmdlet exclui.</span><span class="sxs-lookup"><span data-stu-id="9f93b-117">Specifies the route table that contains the route that this cmdlet deletes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f93b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f93b-118">-DefaultProfile</span></span>
<span data-ttu-id="9f93b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9f93b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f93b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f93b-120">CommonParameters</span></span>
<span data-ttu-id="9f93b-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f93b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f93b-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f93b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f93b-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9f93b-123">INPUTS</span></span>

### <span data-ttu-id="9f93b-124">PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9f93b-124">PSRouteTable</span></span>
<span data-ttu-id="9f93b-125">O parâmetro ' RouteTable ' aceita o valor do tipo ' PSRouteTable ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="9f93b-125">Parameter 'RouteTable' accepts value of type 'PSRouteTable' from the pipeline</span></span>

## <span data-ttu-id="9f93b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9f93b-126">OUTPUTS</span></span>

### <span data-ttu-id="9f93b-127">Microsoft. Azure. Commands. Network. Models. PSRouteTable</span><span class="sxs-lookup"><span data-stu-id="9f93b-127">Microsoft.Azure.Commands.Network.Models.PSRouteTable</span></span>

## <span data-ttu-id="9f93b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9f93b-128">NOTES</span></span>

## <span data-ttu-id="9f93b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f93b-129">RELATED LINKS</span></span>

[<span data-ttu-id="9f93b-130">Add-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9f93b-130">Add-AzureRmRouteConfig</span></span>](./Add-AzureRmRouteConfig.md)

[<span data-ttu-id="9f93b-131">Get-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9f93b-131">Get-AzureRmRouteConfig</span></span>](./Get-AzureRmRouteConfig.md)

[<span data-ttu-id="9f93b-132">New-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9f93b-132">New-AzureRmRouteConfig</span></span>](./New-AzureRmRouteConfig.md)

[<span data-ttu-id="9f93b-133">Set-AzureRmRouteConfig</span><span class="sxs-lookup"><span data-stu-id="9f93b-133">Set-AzureRmRouteConfig</span></span>](./Set-AzureRmRouteConfig.md)


