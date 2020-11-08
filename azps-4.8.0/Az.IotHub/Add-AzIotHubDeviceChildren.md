---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: f6996a97d0e3a9ad654c4ea6aac421c8218c729a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111975"
---
# <span data-ttu-id="4cda3-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="4cda3-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="4cda3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4cda3-102">SYNOPSIS</span></span>
<span data-ttu-id="4cda3-103">Adicione dispositivos fora da borda como filhos ao dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="4cda3-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="4cda3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cda3-104">SYNTAX</span></span>

### <span data-ttu-id="4cda3-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4cda3-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cda3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4cda3-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cda3-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="4cda3-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cda3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4cda3-108">DESCRIPTION</span></span>
<span data-ttu-id="4cda3-109">Adicionar uma lista separada por vírgula especificada de IDs de dispositivo não borda como filhos do dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="4cda3-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="4cda3-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4cda3-110">EXAMPLES</span></span>

### <span data-ttu-id="4cda3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4cda3-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="4cda3-112">Adicione dispositivos fora da borda como filhos ao dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="4cda3-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="4cda3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4cda3-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="4cda3-114">Adicione dispositivos sem borda como filhos ao dispositivo de borda independentemente de o dispositivo que não está em borda já ser filho de outro dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="4cda3-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="4cda3-115">OS</span><span class="sxs-lookup"><span data-stu-id="4cda3-115">PARAMETERS</span></span>

### <span data-ttu-id="4cda3-116">-Filhos</span><span class="sxs-lookup"><span data-stu-id="4cda3-116">-Children</span></span>
<span data-ttu-id="4cda3-117">Lista de dispositivos filho (separados por vírgulas) inclui apenas dispositivos que não estão na borda.</span><span class="sxs-lookup"><span data-stu-id="4cda3-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="4cda3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cda3-118">-DefaultProfile</span></span>
<span data-ttu-id="4cda3-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4cda3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cda3-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="4cda3-120">-DeviceId</span></span>
<span data-ttu-id="4cda3-121">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="4cda3-121">Id of edge device.</span></span>

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

### <span data-ttu-id="4cda3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="4cda3-122">-Force</span></span>
<span data-ttu-id="4cda3-123">Substitui o dispositivo pai do dispositivo não-Edge.</span><span class="sxs-lookup"><span data-stu-id="4cda3-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="4cda3-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cda3-124">-InputObject</span></span>
<span data-ttu-id="4cda3-125">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="4cda3-125">IotHub object</span></span>

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

### <span data-ttu-id="4cda3-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4cda3-126">-IotHubName</span></span>
<span data-ttu-id="4cda3-127">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="4cda3-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4cda3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cda3-128">-ResourceGroupName</span></span>
<span data-ttu-id="4cda3-129">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4cda3-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4cda3-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cda3-130">-ResourceId</span></span>
<span data-ttu-id="4cda3-131">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="4cda3-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4cda3-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4cda3-132">-Confirm</span></span>
<span data-ttu-id="4cda3-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cda3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cda3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cda3-134">-WhatIf</span></span>
<span data-ttu-id="4cda3-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4cda3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cda3-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4cda3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cda3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cda3-137">CommonParameters</span></span>
<span data-ttu-id="4cda3-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cda3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cda3-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cda3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cda3-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4cda3-140">INPUTS</span></span>

### <span data-ttu-id="4cda3-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4cda3-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4cda3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="4cda3-142">System.String</span></span>

## <span data-ttu-id="4cda3-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4cda3-143">OUTPUTS</span></span>

### <span data-ttu-id="4cda3-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="4cda3-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="4cda3-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4cda3-145">NOTES</span></span>

## <span data-ttu-id="4cda3-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4cda3-146">RELATED LINKS</span></span>
