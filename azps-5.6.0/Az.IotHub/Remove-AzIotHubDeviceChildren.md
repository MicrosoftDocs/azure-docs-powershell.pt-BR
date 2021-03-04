---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 296793309dbcae7317353e41f9f3562a020c9be2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893278"
---
# <span data-ttu-id="741b1-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="741b1-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="741b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="741b1-102">SYNOPSIS</span></span>
<span data-ttu-id="741b1-103">Remova dispositivos que não sejam de borda como filhos do dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="741b1-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="741b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="741b1-104">SYNTAX</span></span>

### <span data-ttu-id="741b1-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="741b1-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="741b1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="741b1-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="741b1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="741b1-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="741b1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="741b1-108">DESCRIPTION</span></span>
<span data-ttu-id="741b1-109">Remova todos ou mencionados dispositivos que não sejam de borda como dispositivos de borda especificados para filhos.</span><span class="sxs-lookup"><span data-stu-id="741b1-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="741b1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="741b1-110">EXAMPLES</span></span>

### <span data-ttu-id="741b1-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="741b1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="741b1-112">Remova os dispositivos mencionados como filhos do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="741b1-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="741b1-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="741b1-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="741b1-114">Remova todos os dispositivos que não sejam de borda como filhos dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="741b1-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="741b1-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="741b1-115">PARAMETERS</span></span>

### <span data-ttu-id="741b1-116">-Children</span><span class="sxs-lookup"><span data-stu-id="741b1-116">-Children</span></span>
<span data-ttu-id="741b1-117">A lista de dispositivos filho (vírgula separada) inclui apenas dispositivos que não são de borda.</span><span class="sxs-lookup"><span data-stu-id="741b1-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="741b1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="741b1-118">-DefaultProfile</span></span>
<span data-ttu-id="741b1-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="741b1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="741b1-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="741b1-120">-DeviceId</span></span>
<span data-ttu-id="741b1-121">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="741b1-121">Id of edge device.</span></span>

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

### <span data-ttu-id="741b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="741b1-122">-InputObject</span></span>
<span data-ttu-id="741b1-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="741b1-123">IotHub object</span></span>

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

### <span data-ttu-id="741b1-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="741b1-124">-IotHubName</span></span>
<span data-ttu-id="741b1-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="741b1-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="741b1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="741b1-126">-PassThru</span></span>
<span data-ttu-id="741b1-127">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="741b1-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="741b1-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="741b1-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="741b1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="741b1-129">-ResourceGroupName</span></span>
<span data-ttu-id="741b1-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="741b1-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="741b1-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="741b1-131">-ResourceId</span></span>
<span data-ttu-id="741b1-132">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="741b1-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="741b1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="741b1-133">-Confirm</span></span>
<span data-ttu-id="741b1-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="741b1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="741b1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="741b1-135">-WhatIf</span></span>
<span data-ttu-id="741b1-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="741b1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="741b1-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="741b1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="741b1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="741b1-138">CommonParameters</span></span>
<span data-ttu-id="741b1-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="741b1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="741b1-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="741b1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="741b1-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="741b1-141">INPUTS</span></span>

### <span data-ttu-id="741b1-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="741b1-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="741b1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="741b1-143">System.String</span></span>

## <span data-ttu-id="741b1-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="741b1-144">OUTPUTS</span></span>

### <span data-ttu-id="741b1-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="741b1-145">System.Boolean</span></span>

## <span data-ttu-id="741b1-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="741b1-146">NOTES</span></span>

## <span data-ttu-id="741b1-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="741b1-147">RELATED LINKS</span></span>
