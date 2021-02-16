---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/invoke-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Invoke-AzStackEdgeShare.md
ms.openlocfilehash: 39e695ad33568ca88996428c3e3d972ae693b503
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113689"
---
# <span data-ttu-id="80e26-101">Invoke-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="80e26-101">Invoke-AzStackEdgeShare</span></span>

## <span data-ttu-id="80e26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="80e26-102">SYNOPSIS</span></span>
<span data-ttu-id="80e26-103">Invoca ações específicas em um compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="80e26-103">Invokes specific actions on a share.</span></span>

## <span data-ttu-id="80e26-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="80e26-104">SYNTAX</span></span>

### <span data-ttu-id="80e26-105">InvokeByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="80e26-105">InvokeByNameParameterSet (Default)</span></span>
```
Invoke-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-RefreshData] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="80e26-106">InvokeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="80e26-106">InvokeByResourceIdParameterSet</span></span>
```
Invoke-AzStackEdgeShare -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-RefreshData]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80e26-107">InvokeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="80e26-107">InvokeByInputObjectParameterSet</span></span>
```
Invoke-AzStackEdgeShare [-AsJob] [-DefaultProfile <IAzureContextContainer>] -InputObject <PSStackEdgeShare>
 [-RefreshData] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80e26-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="80e26-108">DESCRIPTION</span></span>
<span data-ttu-id="80e26-109">O cmdlet **Invoke-AzSt stackEdgeShare** invoca a ação para atualizar dados em um compartilhamento em um dispositivo stack edge.</span><span class="sxs-lookup"><span data-stu-id="80e26-109">The **Invoke-AzStackEdgeShare** cmdlet invokes action to refresh data on a share on a Stack Edge device.</span></span>

## <span data-ttu-id="80e26-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="80e26-110">EXAMPLES</span></span>

### <span data-ttu-id="80e26-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="80e26-111">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 -PassThru
PS C:\> true
```

### <span data-ttu-id="80e26-112">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="80e26-112">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name share1 | Invoke-AzStackEdgeShare
```

## <span data-ttu-id="80e26-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80e26-113">PARAMETERS</span></span>

### <span data-ttu-id="80e26-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80e26-114">-AsJob</span></span>
<span data-ttu-id="80e26-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="80e26-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="80e26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80e26-116">-DefaultProfile</span></span>
<span data-ttu-id="80e26-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="80e26-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80e26-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="80e26-118">-DeviceName</span></span>
<span data-ttu-id="80e26-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="80e26-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e26-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80e26-120">-InputObject</span></span>
<span data-ttu-id="80e26-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="80e26-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: InvokeByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80e26-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="80e26-122">-Name</span></span>
<span data-ttu-id="80e26-123">Nome do Recurso</span><span class="sxs-lookup"><span data-stu-id="80e26-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e26-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80e26-124">-PassThru</span></span>
<span data-ttu-id="80e26-125">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="80e26-125">returns true if successful</span></span>

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

### <span data-ttu-id="80e26-126">-RefreshData</span><span class="sxs-lookup"><span data-stu-id="80e26-126">-RefreshData</span></span>
<span data-ttu-id="80e26-127">Atualizar o Compartilhamento de Metadados com os dados da nuvem</span><span class="sxs-lookup"><span data-stu-id="80e26-127">Refresh Share Metadata with the data from the cloud</span></span>

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

### <span data-ttu-id="80e26-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80e26-128">-ResourceGroupName</span></span>
<span data-ttu-id="80e26-129">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="80e26-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e26-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80e26-130">-ResourceId</span></span>
<span data-ttu-id="80e26-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="80e26-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: InvokeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80e26-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="80e26-132">-Confirm</span></span>
<span data-ttu-id="80e26-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80e26-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80e26-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80e26-134">-WhatIf</span></span>
<span data-ttu-id="80e26-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="80e26-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80e26-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="80e26-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80e26-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80e26-137">CommonParameters</span></span>
<span data-ttu-id="80e26-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80e26-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80e26-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80e26-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80e26-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="80e26-140">INPUTS</span></span>

### <span data-ttu-id="80e26-141">System.String</span><span class="sxs-lookup"><span data-stu-id="80e26-141">System.String</span></span>

### <span data-ttu-id="80e26-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="80e26-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="80e26-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="80e26-143">OUTPUTS</span></span>

### <span data-ttu-id="80e26-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80e26-144">System.Boolean</span></span>

## <span data-ttu-id="80e26-145">Notas</span><span class="sxs-lookup"><span data-stu-id="80e26-145">NOTES</span></span>

## <span data-ttu-id="80e26-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="80e26-146">RELATED LINKS</span></span>
