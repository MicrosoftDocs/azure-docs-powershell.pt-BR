---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272821"
---
# <span data-ttu-id="37c4b-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="37c4b-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="37c4b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="37c4b-103">Remover dispositivos fora da borda como filhos do dispositivo de borda especificado.</span><span class="sxs-lookup"><span data-stu-id="37c4b-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="37c4b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37c4b-104">SYNTAX</span></span>

### <span data-ttu-id="37c4b-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="37c4b-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37c4b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="37c4b-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37c4b-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="37c4b-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37c4b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="37c4b-108">DESCRIPTION</span></span>
<span data-ttu-id="37c4b-109">Remova todos os dispositivos não-Edge ou mencionados como dispositivos de borda especificados como filhos.</span><span class="sxs-lookup"><span data-stu-id="37c4b-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="37c4b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="37c4b-110">EXAMPLES</span></span>

### <span data-ttu-id="37c4b-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="37c4b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="37c4b-112">Remova os dispositivos mencionados como filhos do dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="37c4b-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="37c4b-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="37c4b-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="37c4b-114">Remova todos os dispositivos não Edge como dispositivos de borda especificados pelo filho.</span><span class="sxs-lookup"><span data-stu-id="37c4b-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="37c4b-115">OS</span><span class="sxs-lookup"><span data-stu-id="37c4b-115">PARAMETERS</span></span>

### <span data-ttu-id="37c4b-116">-Filhos</span><span class="sxs-lookup"><span data-stu-id="37c4b-116">-Children</span></span>
<span data-ttu-id="37c4b-117">Lista de dispositivos filho (separados por vírgulas) inclui apenas dispositivos que não estão na borda.</span><span class="sxs-lookup"><span data-stu-id="37c4b-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="37c4b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c4b-118">-DefaultProfile</span></span>
<span data-ttu-id="37c4b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37c4b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c4b-120">-DeviceID</span><span class="sxs-lookup"><span data-stu-id="37c4b-120">-DeviceId</span></span>
<span data-ttu-id="37c4b-121">ID do dispositivo de borda.</span><span class="sxs-lookup"><span data-stu-id="37c4b-121">Id of edge device.</span></span>

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

### <span data-ttu-id="37c4b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37c4b-122">-InputObject</span></span>
<span data-ttu-id="37c4b-123">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="37c4b-123">IotHub object</span></span>

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

### <span data-ttu-id="37c4b-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="37c4b-124">-IotHubName</span></span>
<span data-ttu-id="37c4b-125">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="37c4b-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="37c4b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37c4b-126">-PassThru</span></span>
<span data-ttu-id="37c4b-127">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="37c4b-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="37c4b-128">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="37c4b-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="37c4b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37c4b-129">-ResourceGroupName</span></span>
<span data-ttu-id="37c4b-130">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="37c4b-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="37c4b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37c4b-131">-ResourceId</span></span>
<span data-ttu-id="37c4b-132">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="37c4b-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="37c4b-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="37c4b-133">-Confirm</span></span>
<span data-ttu-id="37c4b-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37c4b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37c4b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37c4b-135">-WhatIf</span></span>
<span data-ttu-id="37c4b-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="37c4b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37c4b-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37c4b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37c4b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c4b-138">CommonParameters</span></span>
<span data-ttu-id="37c4b-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c4b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c4b-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37c4b-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c4b-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="37c4b-141">INPUTS</span></span>

### <span data-ttu-id="37c4b-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="37c4b-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="37c4b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="37c4b-143">System.String</span></span>

## <span data-ttu-id="37c4b-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="37c4b-144">OUTPUTS</span></span>

### <span data-ttu-id="37c4b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37c4b-145">System.Boolean</span></span>

## <span data-ttu-id="37c4b-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="37c4b-146">NOTES</span></span>

## <span data-ttu-id="37c4b-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37c4b-147">RELATED LINKS</span></span>
