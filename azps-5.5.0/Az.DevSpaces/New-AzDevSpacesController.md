---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/new-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/New-AzDevSpacesController.md
ms.openlocfilehash: a99a26060492efbe40bc4a16633ca6a207e093b4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127006"
---
# <span data-ttu-id="44d03-101">New-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="44d03-101">New-AzDevSpacesController</span></span>

## <span data-ttu-id="44d03-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="44d03-102">SYNOPSIS</span></span>
<span data-ttu-id="44d03-103">Crie um novo controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="44d03-103">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="44d03-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44d03-104">SYNTAX</span></span>

```
New-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-TargetResourceGroupName] <String>
 [-TargetClusterName] <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44d03-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="44d03-105">DESCRIPTION</span></span>
<span data-ttu-id="44d03-106">Crie um novo controlador do Azure DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="44d03-106">Create a new Azure DevSpaces controller.</span></span>

## <span data-ttu-id="44d03-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44d03-107">EXAMPLES</span></span>

### <span data-ttu-id="44d03-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="44d03-108">Example 1</span></span>
```powershell
PS C:\> New-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -TargetResourceGroupName clusterResourceGroup -TargetClusterName clusterName

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="44d03-109">Crie um controlador DevSpaces no devSpaceResourceGroup de grupo de recursos com um nome devSpaceName.</span><span class="sxs-lookup"><span data-stu-id="44d03-109">Create a DevSpaces controller in resourcegroup devSpaceResourceGroup with a name devSpaceName.</span></span> <span data-ttu-id="44d03-110">Use clusterName cluster como um destino para este controlador.</span><span class="sxs-lookup"><span data-stu-id="44d03-110">Use clusterName cluster as a target for this controller.</span></span>

## <span data-ttu-id="44d03-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44d03-111">PARAMETERS</span></span>

### <span data-ttu-id="44d03-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="44d03-112">-AsJob</span></span>
<span data-ttu-id="44d03-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="44d03-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="44d03-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d03-114">-DefaultProfile</span></span>
<span data-ttu-id="44d03-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="44d03-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44d03-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="44d03-116">-Name</span></span>
<span data-ttu-id="44d03-117">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="44d03-117">DevSpaces Controller Name.</span></span>

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

### <span data-ttu-id="44d03-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d03-118">-ResourceGroupName</span></span>
<span data-ttu-id="44d03-119">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="44d03-119">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d03-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="44d03-120">-Tag</span></span>
<span data-ttu-id="44d03-121">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="44d03-121">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d03-122">-TargetClusterName</span><span class="sxs-lookup"><span data-stu-id="44d03-122">-TargetClusterName</span></span>
<span data-ttu-id="44d03-123">Nome do Cluster de Destino.</span><span class="sxs-lookup"><span data-stu-id="44d03-123">Target Cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d03-124">-TargetResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d03-124">-TargetResourceGroupName</span></span>
<span data-ttu-id="44d03-125">Nome do Grupo de Recursos de Destino.</span><span class="sxs-lookup"><span data-stu-id="44d03-125">Target Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d03-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="44d03-126">-Confirm</span></span>
<span data-ttu-id="44d03-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44d03-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44d03-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44d03-128">-WhatIf</span></span>
<span data-ttu-id="44d03-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="44d03-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44d03-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="44d03-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44d03-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d03-131">CommonParameters</span></span>
<span data-ttu-id="44d03-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d03-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d03-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d03-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d03-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="44d03-134">INPUTS</span></span>

### <span data-ttu-id="44d03-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="44d03-135">None</span></span>

## <span data-ttu-id="44d03-136">Saídas</span><span class="sxs-lookup"><span data-stu-id="44d03-136">OUTPUTS</span></span>

### <span data-ttu-id="44d03-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="44d03-137">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="44d03-138">Notas</span><span class="sxs-lookup"><span data-stu-id="44d03-138">NOTES</span></span>

## <span data-ttu-id="44d03-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="44d03-139">RELATED LINKS</span></span>
