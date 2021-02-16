---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117611"
---
# <span data-ttu-id="71b66-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="71b66-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="71b66-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71b66-102">SYNOPSIS</span></span>
<span data-ttu-id="71b66-103">Remova dispositivos que não são de borda como filhos do dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="71b66-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="71b66-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71b66-104">SYNTAX</span></span>

### <span data-ttu-id="71b66-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="71b66-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71b66-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="71b66-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b66-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="71b66-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71b66-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="71b66-108">DESCRIPTION</span></span>
<span data-ttu-id="71b66-109">Remova todos os dispositivos sem borda mencionados como dispositivos de borda especificados para crianças.</span><span class="sxs-lookup"><span data-stu-id="71b66-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="71b66-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="71b66-110">EXAMPLES</span></span>

### <span data-ttu-id="71b66-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="71b66-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="71b66-112">Remover dispositivos mencionados como filhos de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="71b66-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="71b66-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="71b66-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="71b66-114">Remova todos os dispositivos que não são de borda como dispositivo de borda especificado para crianças.</span><span class="sxs-lookup"><span data-stu-id="71b66-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="71b66-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71b66-115">PARAMETERS</span></span>

### <span data-ttu-id="71b66-116">-Crianças</span><span class="sxs-lookup"><span data-stu-id="71b66-116">-Children</span></span>
<span data-ttu-id="71b66-117">A lista de dispositivos filho (vírgulas separadas) inclui apenas dispositivos que não são de borda.</span><span class="sxs-lookup"><span data-stu-id="71b66-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="71b66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b66-118">-DefaultProfile</span></span>
<span data-ttu-id="71b66-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="71b66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71b66-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="71b66-120">-DeviceId</span></span>
<span data-ttu-id="71b66-121">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="71b66-121">Id of edge device.</span></span>

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

### <span data-ttu-id="71b66-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71b66-122">-InputObject</span></span>
<span data-ttu-id="71b66-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="71b66-123">IotHub object</span></span>

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

### <span data-ttu-id="71b66-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="71b66-124">-IotHubName</span></span>
<span data-ttu-id="71b66-125">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="71b66-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="71b66-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71b66-126">-PassThru</span></span>
<span data-ttu-id="71b66-127">Permite retornar o objeto boolano.</span><span class="sxs-lookup"><span data-stu-id="71b66-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="71b66-128">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="71b66-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71b66-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71b66-129">-ResourceGroupName</span></span>
<span data-ttu-id="71b66-130">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="71b66-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="71b66-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71b66-131">-ResourceId</span></span>
<span data-ttu-id="71b66-132">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="71b66-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="71b66-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="71b66-133">-Confirm</span></span>
<span data-ttu-id="71b66-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71b66-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b66-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b66-135">-WhatIf</span></span>
<span data-ttu-id="71b66-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="71b66-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71b66-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="71b66-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b66-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b66-138">CommonParameters</span></span>
<span data-ttu-id="71b66-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71b66-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b66-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b66-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b66-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="71b66-141">INPUTS</span></span>

### <span data-ttu-id="71b66-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="71b66-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="71b66-143">System.String</span><span class="sxs-lookup"><span data-stu-id="71b66-143">System.String</span></span>

## <span data-ttu-id="71b66-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="71b66-144">OUTPUTS</span></span>

### <span data-ttu-id="71b66-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="71b66-145">System.Boolean</span></span>

## <span data-ttu-id="71b66-146">Notas</span><span class="sxs-lookup"><span data-stu-id="71b66-146">NOTES</span></span>

## <span data-ttu-id="71b66-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71b66-147">RELATED LINKS</span></span>
