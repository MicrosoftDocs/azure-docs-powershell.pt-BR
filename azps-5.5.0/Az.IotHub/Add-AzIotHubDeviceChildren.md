---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113782"
---
# <span data-ttu-id="a1d15-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a1d15-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="a1d15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1d15-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d15-103">Adicione dispositivos que não são de borda como filhos ao dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="a1d15-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="a1d15-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1d15-104">SYNTAX</span></span>

### <span data-ttu-id="a1d15-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a1d15-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1d15-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a1d15-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1d15-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a1d15-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1d15-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1d15-108">DESCRIPTION</span></span>
<span data-ttu-id="a1d15-109">Adicione uma lista especificada separada por vírgulas de IDs de dispositivo não de borda como filhos de dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="a1d15-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="a1d15-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a1d15-110">EXAMPLES</span></span>

### <span data-ttu-id="a1d15-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a1d15-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="a1d15-112">Adicione dispositivos que não são de borda como filhos ao dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="a1d15-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="a1d15-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a1d15-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="a1d15-114">Adicione dispositivos que não são de borda como filhos ao dispositivo de borda independentemente de que o dispositivo sem borda já seja filho de outro dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="a1d15-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="a1d15-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1d15-115">PARAMETERS</span></span>

### <span data-ttu-id="a1d15-116">-Crianças</span><span class="sxs-lookup"><span data-stu-id="a1d15-116">-Children</span></span>
<span data-ttu-id="a1d15-117">A lista de dispositivos filho (vírgulas separadas) inclui apenas dispositivos que não são de borda.</span><span class="sxs-lookup"><span data-stu-id="a1d15-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d15-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d15-118">-DefaultProfile</span></span>
<span data-ttu-id="a1d15-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a1d15-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1d15-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a1d15-120">-DeviceId</span></span>
<span data-ttu-id="a1d15-121">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="a1d15-121">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1d15-122">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a1d15-122">-Force</span></span>
<span data-ttu-id="a1d15-123">Substitui o dispositivo pai do dispositivo sem borda.</span><span class="sxs-lookup"><span data-stu-id="a1d15-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="a1d15-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1d15-124">-InputObject</span></span>
<span data-ttu-id="a1d15-125">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a1d15-125">IotHub object</span></span>

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

### <span data-ttu-id="a1d15-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a1d15-126">-IotHubName</span></span>
<span data-ttu-id="a1d15-127">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="a1d15-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a1d15-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d15-128">-ResourceGroupName</span></span>
<span data-ttu-id="a1d15-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a1d15-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a1d15-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1d15-130">-ResourceId</span></span>
<span data-ttu-id="a1d15-131">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="a1d15-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a1d15-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a1d15-132">-Confirm</span></span>
<span data-ttu-id="a1d15-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1d15-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d15-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d15-134">-WhatIf</span></span>
<span data-ttu-id="a1d15-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a1d15-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1d15-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1d15-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d15-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d15-137">CommonParameters</span></span>
<span data-ttu-id="a1d15-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1d15-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d15-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d15-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d15-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="a1d15-140">INPUTS</span></span>

### <span data-ttu-id="a1d15-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a1d15-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a1d15-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a1d15-142">System.String</span></span>

## <span data-ttu-id="a1d15-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="a1d15-143">OUTPUTS</span></span>

### <span data-ttu-id="a1d15-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="a1d15-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="a1d15-145">Notas</span><span class="sxs-lookup"><span data-stu-id="a1d15-145">NOTES</span></span>

## <span data-ttu-id="a1d15-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1d15-146">RELATED LINKS</span></span>
