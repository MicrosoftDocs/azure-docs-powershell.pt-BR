---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94113558"
---
# <span data-ttu-id="866e4-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="866e4-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="866e4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="866e4-102">SYNOPSIS</span></span>
<span data-ttu-id="866e4-103">Lista todas ou uma implantação de borda IoT específica.</span><span class="sxs-lookup"><span data-stu-id="866e4-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="866e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="866e4-104">SYNTAX</span></span>

### <span data-ttu-id="866e4-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="866e4-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="866e4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="866e4-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="866e4-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="866e4-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="866e4-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="866e4-108">DESCRIPTION</span></span>
<span data-ttu-id="866e4-109">Obter os detalhes de uma implantação de borda IoT ou lista de implantações de borda IoT em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="866e4-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="866e4-110">Consulte https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="866e4-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="866e4-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="866e4-111">EXAMPLES</span></span>

### <span data-ttu-id="866e4-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="866e4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="866e4-113">Obtenha os detalhes de uma implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="866e4-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="866e4-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="866e4-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="866e4-115">Listar todas as implantações de borda IoT em um hub IoT.</span><span class="sxs-lookup"><span data-stu-id="866e4-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="866e4-116">OS</span><span class="sxs-lookup"><span data-stu-id="866e4-116">PARAMETERS</span></span>

### <span data-ttu-id="866e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="866e4-117">-DefaultProfile</span></span>
<span data-ttu-id="866e4-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="866e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="866e4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="866e4-119">-InputObject</span></span>
<span data-ttu-id="866e4-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="866e4-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="866e4-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="866e4-121">-IotHubName</span></span>
<span data-ttu-id="866e4-122">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="866e4-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866e4-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="866e4-123">-Name</span></span>
<span data-ttu-id="866e4-124">Identificador para a implantação.</span><span class="sxs-lookup"><span data-stu-id="866e4-124">Identifier for the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="866e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="866e4-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="866e4-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="866e4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="866e4-127">-ResourceId</span></span>
<span data-ttu-id="866e4-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="866e4-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="866e4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="866e4-129">CommonParameters</span></span>
<span data-ttu-id="866e4-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="866e4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="866e4-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="866e4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="866e4-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="866e4-132">INPUTS</span></span>

### <span data-ttu-id="866e4-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="866e4-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="866e4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="866e4-134">System.String</span></span>

## <span data-ttu-id="866e4-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="866e4-135">OUTPUTS</span></span>

### <span data-ttu-id="866e4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="866e4-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="866e4-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments []</span><span class="sxs-lookup"><span data-stu-id="866e4-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="866e4-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="866e4-138">NOTES</span></span>

## <span data-ttu-id="866e4-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="866e4-139">RELATED LINKS</span></span>
