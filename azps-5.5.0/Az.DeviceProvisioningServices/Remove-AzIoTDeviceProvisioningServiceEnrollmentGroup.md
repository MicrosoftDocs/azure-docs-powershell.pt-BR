---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115813"
---
# <span data-ttu-id="31cb3-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="31cb3-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="31cb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="31cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="31cb3-103">Excluir um grupo de registro de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31cb3-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="31cb3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31cb3-104">SYNTAX</span></span>

### <span data-ttu-id="31cb3-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="31cb3-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31cb3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="31cb3-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="31cb3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="31cb3-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31cb3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="31cb3-108">DESCRIPTION</span></span>
<span data-ttu-id="31cb3-109">Exclua um grupo de inscrição em um Serviço de Provisionamento de Dispositivo do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="31cb3-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="31cb3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31cb3-110">EXAMPLES</span></span>

### <span data-ttu-id="31cb3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="31cb3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="31cb3-112">Exclua um grupo de inscrição especificado.</span><span class="sxs-lookup"><span data-stu-id="31cb3-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="31cb3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="31cb3-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="31cb3-114">Exclua todos os grupos de inscrição.</span><span class="sxs-lookup"><span data-stu-id="31cb3-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="31cb3-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31cb3-115">PARAMETERS</span></span>

### <span data-ttu-id="31cb3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31cb3-116">-DefaultProfile</span></span>
<span data-ttu-id="31cb3-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="31cb3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31cb3-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="31cb3-118">-DpsName</span></span>
<span data-ttu-id="31cb3-119">Nome do Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="31cb3-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="31cb3-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="31cb3-120">-DpsObject</span></span>
<span data-ttu-id="31cb3-121">Objeto de Serviço de Provisionamento de Dispositivo IoT</span><span class="sxs-lookup"><span data-stu-id="31cb3-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="31cb3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="31cb3-122">-Name</span></span>
<span data-ttu-id="31cb3-123">Nome do grupo de inscrição.</span><span class="sxs-lookup"><span data-stu-id="31cb3-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="31cb3-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31cb3-124">-PassThru</span></span>
<span data-ttu-id="31cb3-125">Permite retornar o objeto boolano.</span><span class="sxs-lookup"><span data-stu-id="31cb3-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="31cb3-126">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="31cb3-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31cb3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31cb3-127">-ResourceGroupName</span></span>
<span data-ttu-id="31cb3-128">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="31cb3-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="31cb3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31cb3-129">-ResourceId</span></span>
<span data-ttu-id="31cb3-130">IoT Device Provisioning Service Resource Id</span><span class="sxs-lookup"><span data-stu-id="31cb3-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="31cb3-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="31cb3-131">-Confirm</span></span>
<span data-ttu-id="31cb3-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31cb3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31cb3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31cb3-133">-WhatIf</span></span>
<span data-ttu-id="31cb3-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="31cb3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31cb3-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="31cb3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31cb3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31cb3-136">CommonParameters</span></span>
<span data-ttu-id="31cb3-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31cb3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31cb3-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31cb3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31cb3-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="31cb3-139">INPUTS</span></span>

### <span data-ttu-id="31cb3-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="31cb3-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="31cb3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="31cb3-141">System.String</span></span>

## <span data-ttu-id="31cb3-142">Saídas</span><span class="sxs-lookup"><span data-stu-id="31cb3-142">OUTPUTS</span></span>

### <span data-ttu-id="31cb3-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="31cb3-143">System.Boolean</span></span>

## <span data-ttu-id="31cb3-144">Notas</span><span class="sxs-lookup"><span data-stu-id="31cb3-144">NOTES</span></span>

## <span data-ttu-id="31cb3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="31cb3-145">RELATED LINKS</span></span>
