---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257515"
---
# <span data-ttu-id="89e56-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="89e56-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="89e56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="89e56-102">SYNOPSIS</span></span>
<span data-ttu-id="89e56-103">Exclua um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="89e56-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="89e56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="89e56-104">SYNTAX</span></span>

### <span data-ttu-id="89e56-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="89e56-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89e56-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="89e56-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89e56-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="89e56-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89e56-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="89e56-108">DESCRIPTION</span></span>
<span data-ttu-id="89e56-109">Excluir um grupo de inscrição em um serviço de provisionamento de dispositivo Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="89e56-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="89e56-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="89e56-110">EXAMPLES</span></span>

### <span data-ttu-id="89e56-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="89e56-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="89e56-112">Excluir um grupo de registros especificado.</span><span class="sxs-lookup"><span data-stu-id="89e56-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="89e56-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="89e56-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="89e56-114">Exclua todos os grupos de inscrição.</span><span class="sxs-lookup"><span data-stu-id="89e56-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="89e56-115">OS</span><span class="sxs-lookup"><span data-stu-id="89e56-115">PARAMETERS</span></span>

### <span data-ttu-id="89e56-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e56-116">-DefaultProfile</span></span>
<span data-ttu-id="89e56-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="89e56-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89e56-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="89e56-118">-DpsName</span></span>
<span data-ttu-id="89e56-119">Nome do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="89e56-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="89e56-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="89e56-120">-DpsObject</span></span>
<span data-ttu-id="89e56-121">Objeto do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="89e56-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e56-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="89e56-122">-Name</span></span>
<span data-ttu-id="89e56-123">Nome do grupo de registro.</span><span class="sxs-lookup"><span data-stu-id="89e56-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="89e56-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="89e56-124">-PassThru</span></span>
<span data-ttu-id="89e56-125">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="89e56-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="89e56-126">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="89e56-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e56-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89e56-127">-ResourceGroupName</span></span>
<span data-ttu-id="89e56-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="89e56-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="89e56-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89e56-129">-ResourceId</span></span>
<span data-ttu-id="89e56-130">ID do recurso do serviço de provisionamento de dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="89e56-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="89e56-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="89e56-131">-Confirm</span></span>
<span data-ttu-id="89e56-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89e56-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e56-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e56-133">-WhatIf</span></span>
<span data-ttu-id="89e56-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="89e56-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89e56-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="89e56-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e56-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e56-136">CommonParameters</span></span>
<span data-ttu-id="89e56-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e56-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e56-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89e56-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e56-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="89e56-139">INPUTS</span></span>

### <span data-ttu-id="89e56-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="89e56-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="89e56-141">System. String</span><span class="sxs-lookup"><span data-stu-id="89e56-141">System.String</span></span>

## <span data-ttu-id="89e56-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="89e56-142">OUTPUTS</span></span>

### <span data-ttu-id="89e56-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="89e56-143">System.Boolean</span></span>

## <span data-ttu-id="89e56-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="89e56-144">NOTES</span></span>

## <span data-ttu-id="89e56-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="89e56-145">RELATED LINKS</span></span>
