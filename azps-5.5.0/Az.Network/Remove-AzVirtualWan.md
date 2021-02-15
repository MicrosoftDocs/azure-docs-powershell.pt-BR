---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualWan.md
ms.openlocfilehash: 802a87b4ba420fb84036756185c68a6250e70920
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111571"
---
# <span data-ttu-id="69044-101">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="69044-101">Remove-AzVirtualWan</span></span>

## <span data-ttu-id="69044-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="69044-102">SYNOPSIS</span></span>
<span data-ttu-id="69044-103">Remove uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="69044-103">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="69044-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="69044-104">SYNTAX</span></span>

### <span data-ttu-id="69044-105">ByVirtualWanName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="69044-105">ByVirtualWanName (Default)</span></span>
```
Remove-AzVirtualWan -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69044-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="69044-106">ByVirtualWanObject</span></span>
```
Remove-AzVirtualWan -InputObject <PSVirtualWan> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69044-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="69044-107">ByVirtualWanResourceId</span></span>
```
Remove-AzVirtualWan -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69044-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="69044-108">DESCRIPTION</span></span>
<span data-ttu-id="69044-109">Remove uma WAN virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="69044-109">Removes an Azure Virtual WAN.</span></span>

## <span data-ttu-id="69044-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="69044-110">EXAMPLES</span></span>

### <span data-ttu-id="69044-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="69044-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Passthru
```

<span data-ttu-id="69044-112">Este exemplo cria uma WAN Virtual em um grupo de recursos e a exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="69044-112">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="69044-113">Para suprimir o prompt ao excluir a WAN Virtual, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="69044-113">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="69044-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="69044-114">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -InputObject $virtualWan -Passthru
```

<span data-ttu-id="69044-115">Este exemplo cria uma WAN Virtual em um grupo de recursos e a exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="69044-115">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="69044-116">Essa exclusão acontece usando o objeto wan virtual retornado por New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="69044-116">This deletion happens using the virtual wan object returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="69044-117">Para suprimir o prompt ao excluir a WAN Virtual, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="69044-117">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

### <span data-ttu-id="69044-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="69044-118">Example 3</span></span>

```powershell
PS C:\> New-AzResourceGroup -Name "TestResourceGroup" -Location "Central US"
PS C:\> $virtualWan = New-AzVirtualWan -Name "MyVirtualWan" -ResourceGroupName "TestResourceGroup" -Location "Central US"
PS C:\> Remove-AzVirtualWan -ResourceId $virtualWan.Id -Passthru
```

<span data-ttu-id="69044-119">Este exemplo cria uma WAN Virtual em um grupo de recursos e a exclui imediatamente.</span><span class="sxs-lookup"><span data-stu-id="69044-119">This example creates a Virtual WAN in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="69044-120">Essa exclusão acontece usando a ID de recurso de wan virtual retornada por New-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="69044-120">This deletion happens using the virtual wan resource id returned by New-AzVirtualWan.</span></span>
<span data-ttu-id="69044-121">Para suprimir o prompt ao excluir a WAN Virtual, use o sinalizador -Force.</span><span class="sxs-lookup"><span data-stu-id="69044-121">To suppress the prompt when deleting the Virtual WAN, use the -Force flag.</span></span>

## <span data-ttu-id="69044-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69044-122">PARAMETERS</span></span>

### <span data-ttu-id="69044-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69044-123">-DefaultProfile</span></span>
<span data-ttu-id="69044-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="69044-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69044-125">-Forçar</span><span class="sxs-lookup"><span data-stu-id="69044-125">-Force</span></span>
<span data-ttu-id="69044-126">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="69044-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="69044-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69044-127">-InputObject</span></span>
<span data-ttu-id="69044-128">O objeto wan virtual a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="69044-128">The virtual wan object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69044-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="69044-129">-Name</span></span>
<span data-ttu-id="69044-130">O nome de wan virtual.</span><span class="sxs-lookup"><span data-stu-id="69044-130">The virtual wan name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69044-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69044-131">-PassThru</span></span>
<span data-ttu-id="69044-132">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="69044-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69044-133">Por padrão, esse cmdlet não gera saída.</span><span class="sxs-lookup"><span data-stu-id="69044-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="69044-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69044-134">-ResourceGroupName</span></span>
<span data-ttu-id="69044-135">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="69044-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69044-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69044-136">-ResourceId</span></span>
<span data-ttu-id="69044-137">A ID de recurso do Azure para a wan virtual ser excluída.</span><span class="sxs-lookup"><span data-stu-id="69044-137">The Azure resource ID for the virtual wan to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69044-138">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="69044-138">-Confirm</span></span>
<span data-ttu-id="69044-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69044-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69044-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69044-140">-WhatIf</span></span>
<span data-ttu-id="69044-141">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="69044-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69044-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="69044-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69044-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69044-143">CommonParameters</span></span>
<span data-ttu-id="69044-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69044-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69044-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69044-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69044-146">Entradas</span><span class="sxs-lookup"><span data-stu-id="69044-146">INPUTS</span></span>

### <span data-ttu-id="69044-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="69044-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="69044-148">System.String</span><span class="sxs-lookup"><span data-stu-id="69044-148">System.String</span></span>

## <span data-ttu-id="69044-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="69044-149">OUTPUTS</span></span>

### <span data-ttu-id="69044-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69044-150">System.Boolean</span></span>

## <span data-ttu-id="69044-151">Notas</span><span class="sxs-lookup"><span data-stu-id="69044-151">NOTES</span></span>

## <span data-ttu-id="69044-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="69044-152">RELATED LINKS</span></span>

[<span data-ttu-id="69044-153">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="69044-153">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="69044-154">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="69044-154">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="69044-155">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="69044-155">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
