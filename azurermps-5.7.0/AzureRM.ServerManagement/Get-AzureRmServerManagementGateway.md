---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: C579BF90-FD8B-4384-96EB-46154E308492
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/get-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9dc7e38cf169e79ec7dae279c6fa09f069b1ade7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426608"
---
# <span data-ttu-id="973fc-101">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="973fc-101">Get-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="973fc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="973fc-102">SYNOPSIS</span></span>
<span data-ttu-id="973fc-103">Obtém um ou mais gateways de gerenciamento do servidor.</span><span class="sxs-lookup"><span data-stu-id="973fc-103">Gets one or more Server Management Gateways.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="973fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="973fc-104">SYNTAX</span></span>

### <span data-ttu-id="973fc-105">Noparams (padrão)</span><span class="sxs-lookup"><span data-stu-id="973fc-105">NoParams (Default)</span></span>
```
Get-AzureRmServerManagementGateway [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="973fc-106">Many-ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="973fc-106">Many-ByResourceGroup</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="973fc-107">Single-ByName</span><span class="sxs-lookup"><span data-stu-id="973fc-107">Single-ByName</span></span>
```
Get-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="973fc-108">Single-ByObject</span><span class="sxs-lookup"><span data-stu-id="973fc-108">Single-ByObject</span></span>
```
Get-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="973fc-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="973fc-109">DESCRIPTION</span></span>
<span data-ttu-id="973fc-110">O cmdlet **Get-AzureRmServerManagementGateway** Obtém um ou mais gateways de gerenciamento do servidor do Azure.</span><span class="sxs-lookup"><span data-stu-id="973fc-110">The **Get-AzureRmServerManagementGateway** cmdlet gets one or more Azure Server Management Gateways.</span></span>

## <span data-ttu-id="973fc-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="973fc-111">EXAMPLES</span></span>

### <span data-ttu-id="973fc-112">Exemplo 1: obter todos os gateways em uma assinatura</span><span class="sxs-lookup"><span data-stu-id="973fc-112">Example 1: Get all gateways in a subscription</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
groupOne       centralus      Off          mygateway
groupOne       centralus      Off          othergateway
groupTwo       centralus      On           privategateway
```

<span data-ttu-id="973fc-113">Esse comando obtém todos os gateways de gerenciamento do servidor na assinatura.</span><span class="sxs-lookup"><span data-stu-id="973fc-113">This command gets all Server Management Gateways in the subscription.</span></span>

### <span data-ttu-id="973fc-114">Exemplo 2: obter gateways em um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="973fc-114">Example 2: Get gateways in a resource group</span></span>
```
PS C:\>Get-AzureRmServerManagementGateway -ResourceGroupName "Group001"
Resource Group Location       Auto Upgrade Gateway Name
-------------- --------       ------------ ------------
myGroup        centralus      Off          mygateway
```

<span data-ttu-id="973fc-115">Esse comando obtém todos os gateways de gerenciamento do servidor que pertencem ao grupo de recursos chamado Group001.</span><span class="sxs-lookup"><span data-stu-id="973fc-115">This command gets all Server Management Gateways that belong to the resource group named Group001.</span></span>

### <span data-ttu-id="973fc-116">Exemplo 3: obter todas as instâncias instaladas de um gateway</span><span class="sxs-lookup"><span data-stu-id="973fc-116">Example 3: Get all installed instances of a gateway</span></span>
```
PS C:\>(Get-AzureRmServerManagementGateway -ResourceGroupName "Group002" -GatewayName "Gateway01").Instances
Name             Installed              Version         Operating System
----             ---------              -------         ----------------
GATEWAYPC        4/13/2016 6:35:04 PM   1.0.1104.0      Microsoft Windows 10 Enterprise
```

<span data-ttu-id="973fc-117">Esse comando obtém todas as instâncias de um gateway de gerenciamento de servidor chamado Gateway01 que pertencem ao grupo de recursos chamado Group002.</span><span class="sxs-lookup"><span data-stu-id="973fc-117">This command gets all instances of a Server Management Gateway named Gateway01 that belong to the resource group named Group002.</span></span>

## <span data-ttu-id="973fc-118">OS</span><span class="sxs-lookup"><span data-stu-id="973fc-118">PARAMETERS</span></span>

### <span data-ttu-id="973fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973fc-119">-DefaultProfile</span></span>
<span data-ttu-id="973fc-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="973fc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="973fc-121">-Gateway</span><span class="sxs-lookup"><span data-stu-id="973fc-121">-Gateway</span></span>
<span data-ttu-id="973fc-122">Especifica um gateway que esse cmdlet obtém.</span><span class="sxs-lookup"><span data-stu-id="973fc-122">Specifies a gateway that this cmdlet gets.</span></span>

<span data-ttu-id="973fc-123">O cmdlet usa os parâmetros *ResourceGroupName* e *GATEWAYNAME* por meio do gateway especificado para executar a ação.</span><span class="sxs-lookup"><span data-stu-id="973fc-123">The cmdlet uses the *ResourceGroupName* and *GatewayName* parameters through the specified Gateway to perform the action.</span></span>

<span data-ttu-id="973fc-124">Quando esse parâmetro for especificado, esse cmdlet incluirá o status detalhado para o gateway.</span><span class="sxs-lookup"><span data-stu-id="973fc-124">When this parameter is specified, this cmdlet will include detailed status for the gateway.</span></span>

```yaml
Type: Gateway
Parameter Sets: Single-ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="973fc-125">-GATEWAYNAME</span><span class="sxs-lookup"><span data-stu-id="973fc-125">-GatewayName</span></span>
<span data-ttu-id="973fc-126">Especifica o nome do gateway de gerenciamento do servidor para o qual esse cmdlet tem portão.</span><span class="sxs-lookup"><span data-stu-id="973fc-126">Specifies the name of the Server Management Gateway for which this cmdlet gets gate.</span></span>

<span data-ttu-id="973fc-127">Quando você especifica o parâmetro *GATEWAYNAME* , esse cmdlet incluirá o status detalhado no gateway.</span><span class="sxs-lookup"><span data-stu-id="973fc-127">When you specify the *GatewayName* parameter, this cmdlet will include detailed status on the gateway.</span></span>

```yaml
Type: String
Parameter Sets: Single-ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="973fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="973fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="973fc-129">Especifica o nome do grupo de recursos para o qual esse cmdlet obtém gateways.</span><span class="sxs-lookup"><span data-stu-id="973fc-129">Specifies the name of the resource group for which this cmdlet gets gateways.</span></span>

```yaml
Type: String
Parameter Sets: Many-ByResourceGroup, Single-ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="973fc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973fc-130">CommonParameters</span></span>
<span data-ttu-id="973fc-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="973fc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973fc-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="973fc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973fc-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="973fc-133">INPUTS</span></span>

### <span data-ttu-id="973fc-134">Gateway</span><span class="sxs-lookup"><span data-stu-id="973fc-134">Gateway</span></span>
<span data-ttu-id="973fc-135">O parâmetro ' gateway ' aceita o valor do tipo ' gateway ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="973fc-135">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="973fc-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="973fc-136">OUTPUTS</span></span>

### <span data-ttu-id="973fc-137">Microsoft. Azure. Commands. ServerManagement. Model. gateway</span><span class="sxs-lookup"><span data-stu-id="973fc-137">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="973fc-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="973fc-138">NOTES</span></span>
* <span data-ttu-id="973fc-139">Se esse cmdlet for usado sem parâmetros, será retornado todos os gateways associados à assinatura.</span><span class="sxs-lookup"><span data-stu-id="973fc-139">If this cmdlet is use without parameters, it will return all the gateways associated with the subscription.</span></span>

## <span data-ttu-id="973fc-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="973fc-140">RELATED LINKS</span></span>

[<span data-ttu-id="973fc-141">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="973fc-141">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)

[<span data-ttu-id="973fc-142">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="973fc-142">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


