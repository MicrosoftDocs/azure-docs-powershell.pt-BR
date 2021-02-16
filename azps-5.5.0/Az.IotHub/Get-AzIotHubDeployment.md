---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeployment.md
ms.openlocfilehash: 1440b77d753a27b1c2a7176be5b44ef69fca2e50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113159"
---
# <span data-ttu-id="4f18f-101">Get-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="4f18f-101">Get-AzIotHubDeployment</span></span>

## <span data-ttu-id="4f18f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f18f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f18f-103">Lista toda ou uma implantação específica de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="4f18f-103">Lists all or a particular IoT Edge deployment.</span></span>

## <span data-ttu-id="4f18f-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f18f-104">SYNTAX</span></span>

### <span data-ttu-id="4f18f-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4f18f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f18f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f18f-106">InputObjectSet</span></span>
```
Get-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4f18f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f18f-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f18f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f18f-108">DESCRIPTION</span></span>
<span data-ttu-id="4f18f-109">Obter os detalhes de uma implantação de Borda IoT ou implantações de Borda de Lista IoT em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="4f18f-109">Get the details of an IoT Edge deployment or List IoT Edge deployments in an IoT Hub.</span></span>
<span data-ttu-id="4f18f-110">Confira https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring mais informações.</span><span class="sxs-lookup"><span data-stu-id="4f18f-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="4f18f-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4f18f-111">EXAMPLES</span></span>

### <span data-ttu-id="4f18f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f18f-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="4f18f-113">Obter os detalhes de uma implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="4f18f-113">Get the details of an IoT Edge deployment.</span></span>

### <span data-ttu-id="4f18f-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4f18f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="4f18f-115">Listar todas as implantações de borda de IoT em um Hub de IoT.</span><span class="sxs-lookup"><span data-stu-id="4f18f-115">List all IoT Edge deployments in an IoT Hub.</span></span>

## <span data-ttu-id="4f18f-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f18f-116">PARAMETERS</span></span>

### <span data-ttu-id="4f18f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f18f-117">-DefaultProfile</span></span>
<span data-ttu-id="4f18f-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4f18f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f18f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f18f-119">-InputObject</span></span>
<span data-ttu-id="4f18f-120">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="4f18f-120">IotHub object</span></span>

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

### <span data-ttu-id="4f18f-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4f18f-121">-IotHubName</span></span>
<span data-ttu-id="4f18f-122">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="4f18f-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4f18f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="4f18f-123">-Name</span></span>
<span data-ttu-id="4f18f-124">Identificador da implantação.</span><span class="sxs-lookup"><span data-stu-id="4f18f-124">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="4f18f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f18f-125">-ResourceGroupName</span></span>
<span data-ttu-id="4f18f-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="4f18f-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4f18f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f18f-127">-ResourceId</span></span>
<span data-ttu-id="4f18f-128">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="4f18f-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4f18f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f18f-129">CommonParameters</span></span>
<span data-ttu-id="4f18f-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f18f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f18f-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f18f-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f18f-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="4f18f-132">INPUTS</span></span>

### <span data-ttu-id="4f18f-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4f18f-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4f18f-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4f18f-134">System.String</span></span>

## <span data-ttu-id="4f18f-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="4f18f-135">OUTPUTS</span></span>

### <span data-ttu-id="4f18f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="4f18f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

### <span data-ttu-id="4f18f-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span><span class="sxs-lookup"><span data-stu-id="4f18f-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployments[]</span></span>

## <span data-ttu-id="4f18f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="4f18f-138">NOTES</span></span>

## <span data-ttu-id="4f18f-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f18f-139">RELATED LINKS</span></span>
