---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 6b98f4266e730e1cfb60ef51046e6846f24999d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602691"
---
# <span data-ttu-id="1059d-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1059d-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="1059d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1059d-102">SYNOPSIS</span></span>
<span data-ttu-id="1059d-103">Obtém um ou mais gateways de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="1059d-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1059d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1059d-104">SYNTAX</span></span>

### <span data-ttu-id="1059d-105">Noparams (padrão)</span><span class="sxs-lookup"><span data-stu-id="1059d-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1059d-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1059d-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1059d-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="1059d-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1059d-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="1059d-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1059d-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1059d-109">DESCRIPTION</span></span>
<span data-ttu-id="1059d-110">O cmdlet **Get-AzureRmServerManagementGateway** Obtém um ou mais gateways de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="1059d-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="1059d-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1059d-111">EXAMPLES</span></span>

### <span data-ttu-id="1059d-112">Exemplo 1: obter todos os gateways em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="1059d-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="1059d-113">Esse comando obtém todos os gateways de gerenciamento do servidor na assinatura.</span><span class="sxs-lookup"><span data-stu-id="1059d-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="1059d-114">Exemplo 2: obter gateways em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1059d-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="1059d-115">Esse comando obtém todos os gateways de gerenciamento do servidor que pertencem ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="1059d-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="1059d-116">Exemplo 3: obter todas as instâncias instaladas de um gateway</span><span class="sxs-lookup"><span data-stu-id="1059d-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="1059d-117">Esse comando obtém todas as instâncias de um gateway de gerenciamento de servidor chamado Gateway01 que pertencem ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="1059d-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="1059d-118">OS</span><span class="sxs-lookup"><span data-stu-id="1059d-118">PARAMETERS</span></span>

### <span data-ttu-id="1059d-119">-Gateway</span><span class="sxs-lookup"><span data-stu-id="1059d-119">-Gateway</span></span>
<span data-ttu-id="1059d-120">Especifica um gateway que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="1059d-120">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="1059d-121">O cmdlet usa os parâmetros *ResourceGroupName* e *GATEWAYNAME* por meio do gateway especificado para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="1059d-121">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="1059d-122">Quando esse parâmetro for especificado, esse cmdlet incluirá o status detalhado para o gateway.</span><span class="sxs-lookup"><span data-stu-id="1059d-122">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1059d-123">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="1059d-123">-GatewayName</span></span>
<span data-ttu-id="1059d-124">Especifica o nome do gateway de gerenciamento do servidor para o qual esse cmdlet tem portão.</span><span class="sxs-lookup"><span data-stu-id="1059d-124">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="1059d-125">Quando você especifica o parâmetro *GATEWAYNAME* , esse cmdlet incluirá o status detalhado no gateway.</span><span class="sxs-lookup"><span data-stu-id="1059d-125">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1059d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1059d-126">-ResourceGroupName</span></span>
<span data-ttu-id="1059d-127">Especifica o nome do grupo de recursos para o qual esse cmdlet obtém gateways.</span><span class="sxs-lookup"><span data-stu-id="1059d-127">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: System.String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1059d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1059d-128">-DefaultProfile</span></span>
<span data-ttu-id="1059d-129">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1059d-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1059d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1059d-130">CommonParameters</span></span>
<span data-ttu-id="1059d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1059d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1059d-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1059d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1059d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1059d-133">INPUTS</span></span>

### <span data-ttu-id="1059d-134">Gateway</span><span class="sxs-lookup"><span data-stu-id="1059d-134">Gateway</span></span>
<span data-ttu-id="1059d-135">O parâmetro ' gateway ' aceita o valor do tipo ' gateway ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="1059d-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="1059d-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1059d-136">OUTPUTS</span></span>

### <span data-ttu-id="1059d-137">Microsoft. Azure. Commands. ServerManagement. Model. gateway</span><span class="sxs-lookup"><span data-stu-id="1059d-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="1059d-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1059d-138">NOTES</span></span>
* <span data-ttu-id="1059d-139">Se esse cmdlet for usado sem parâmetros, será retornado todos os gateways associados à assinatura.</span><span class="sxs-lookup"><span data-stu-id="1059d-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="1059d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1059d-140">RELATED LINKS</span></span>

[<span data-ttu-id="1059d-141">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1059d-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="1059d-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1059d-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


