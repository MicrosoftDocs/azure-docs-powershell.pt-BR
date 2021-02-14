---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeUser.md
ms.openlocfilehash: ec8703b5b107758a331407d431f871acf249885d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115676"
---
# <span data-ttu-id="95d85-101">Remove-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="95d85-101">Remove-AzStackEdgeUser</span></span>

## <span data-ttu-id="95d85-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95d85-102">SYNOPSIS</span></span>
<span data-ttu-id="95d85-103">Remove um usuário em um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95d85-103">Removes a user on a device.</span></span>

## <span data-ttu-id="95d85-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95d85-104">SYNTAX</span></span>

### <span data-ttu-id="95d85-105">DeleteByNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="95d85-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d85-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d85-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d85-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d85-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeUser [-InputObject] <PSStackEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d85-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="95d85-108">DESCRIPTION</span></span>
<span data-ttu-id="95d85-109">O cmdlet **Remove-AzSt stackEdgeUser** remove um usuário no dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="95d85-109">The **Remove-AzStackEdgeUser** cmdlet removes a user on the Stack Edge device.</span></span> <span data-ttu-id="95d85-110">Há suporte para a criação de apenas usuários `Share` do tipo.</span><span class="sxs-lookup"><span data-stu-id="95d85-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="95d85-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="95d85-111">EXAMPLES</span></span>

### <span data-ttu-id="95d85-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="95d85-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="95d85-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="95d85-113">PARAMETERS</span></span>

### <span data-ttu-id="95d85-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95d85-114">-AsJob</span></span>
<span data-ttu-id="95d85-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="95d85-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95d85-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d85-116">-DefaultProfile</span></span>
<span data-ttu-id="95d85-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95d85-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95d85-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="95d85-118">-DeviceName</span></span>
<span data-ttu-id="95d85-119">Nome do dispositivo</span><span class="sxs-lookup"><span data-stu-id="95d85-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d85-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95d85-120">-InputObject</span></span>
<span data-ttu-id="95d85-121">Objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="95d85-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: User

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95d85-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="95d85-122">-Name</span></span>
<span data-ttu-id="95d85-123">Username</span><span class="sxs-lookup"><span data-stu-id="95d85-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d85-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95d85-124">-PassThru</span></span>
<span data-ttu-id="95d85-125">retorna verdadeiro se for bem-sucedido</span><span class="sxs-lookup"><span data-stu-id="95d85-125">returns true if successful</span></span>

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

### <span data-ttu-id="95d85-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95d85-126">-ResourceGroupName</span></span>
<span data-ttu-id="95d85-127">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="95d85-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d85-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95d85-128">-ResourceId</span></span>
<span data-ttu-id="95d85-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="95d85-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d85-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="95d85-130">-Confirm</span></span>
<span data-ttu-id="95d85-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95d85-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d85-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d85-132">-WhatIf</span></span>
<span data-ttu-id="95d85-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="95d85-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95d85-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95d85-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d85-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d85-135">CommonParameters</span></span>
<span data-ttu-id="95d85-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95d85-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d85-137">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95d85-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d85-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="95d85-138">INPUTS</span></span>

### <span data-ttu-id="95d85-139">System.String</span><span class="sxs-lookup"><span data-stu-id="95d85-139">System.String</span></span>

### <span data-ttu-id="95d85-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="95d85-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="95d85-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="95d85-141">OUTPUTS</span></span>

### <span data-ttu-id="95d85-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSSt stackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="95d85-142">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="95d85-143">Notas</span><span class="sxs-lookup"><span data-stu-id="95d85-143">NOTES</span></span>

## <span data-ttu-id="95d85-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95d85-144">RELATED LINKS</span></span>
