---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: dc8b22697d606e827a0855a446d969ff2c90edc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595747"
---
# <span data-ttu-id="3738a-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="3738a-101">Remove-AzAks</span></span>

## <span data-ttu-id="3738a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3738a-102">SYNOPSIS</span></span>
<span data-ttu-id="3738a-103">Excluir um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3738a-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3738a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3738a-104">SYNTAX</span></span>

### <span data-ttu-id="3738a-105">GroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3738a-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3738a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3738a-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3738a-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3738a-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3738a-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3738a-108">DESCRIPTION</span></span>
<span data-ttu-id="3738a-109">Excluir um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="3738a-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="3738a-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3738a-110">EXAMPLES</span></span>

### <span data-ttu-id="3738a-111">Excluir um cluster de kubernetes gerenciado existente</span><span class="sxs-lookup"><span data-stu-id="3738a-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="3738a-112">OS</span><span class="sxs-lookup"><span data-stu-id="3738a-112">PARAMETERS</span></span>

### <span data-ttu-id="3738a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3738a-113">-AsJob</span></span>
<span data-ttu-id="3738a-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3738a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3738a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3738a-115">-DefaultProfile</span></span>
<span data-ttu-id="3738a-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3738a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3738a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="3738a-117">-Force</span></span>
<span data-ttu-id="3738a-118">Remover o cluster gerenciado kubernetes sem perguntar</span><span class="sxs-lookup"><span data-stu-id="3738a-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="3738a-119">-ID</span><span class="sxs-lookup"><span data-stu-id="3738a-119">-Id</span></span>
<span data-ttu-id="3738a-120">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="3738a-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3738a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3738a-121">-InputObject</span></span>
<span data-ttu-id="3738a-122">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3738a-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3738a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="3738a-123">-Name</span></span>
<span data-ttu-id="3738a-124">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="3738a-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3738a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3738a-125">-PassThru</span></span>
<span data-ttu-id="3738a-126">Retorna verdadeiro se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="3738a-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="3738a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3738a-127">-ResourceGroupName</span></span>
<span data-ttu-id="3738a-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3738a-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3738a-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3738a-129">-Confirm</span></span>
<span data-ttu-id="3738a-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3738a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3738a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3738a-131">-WhatIf</span></span>
<span data-ttu-id="3738a-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3738a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3738a-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3738a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3738a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3738a-134">CommonParameters</span></span>
<span data-ttu-id="3738a-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3738a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3738a-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3738a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3738a-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3738a-137">INPUTS</span></span>

### <span data-ttu-id="3738a-138">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="3738a-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="3738a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3738a-139">System.String</span></span>

## <span data-ttu-id="3738a-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3738a-140">OUTPUTS</span></span>

### <span data-ttu-id="3738a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3738a-141">System.Boolean</span></span>

## <span data-ttu-id="3738a-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3738a-142">NOTES</span></span>

## <span data-ttu-id="3738a-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3738a-143">RELATED LINKS</span></span>
