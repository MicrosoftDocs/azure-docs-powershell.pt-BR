---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 1843322f702f8c43f97f1cf64c9d9f5b92d419bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432528"
---
# <span data-ttu-id="0745d-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="0745d-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="0745d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0745d-102">SYNOPSIS</span></span>
<span data-ttu-id="0745d-103">Excluir um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0745d-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0745d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0745d-104">SYNTAX</span></span>

### <span data-ttu-id="0745d-105">GroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0745d-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0745d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0745d-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0745d-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0745d-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0745d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0745d-108">DESCRIPTION</span></span>
<span data-ttu-id="0745d-109">Excluir um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="0745d-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="0745d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0745d-110">EXAMPLES</span></span>

### <span data-ttu-id="0745d-111">Excluir um cluster de kubernetes gerenciado existente</span><span class="sxs-lookup"><span data-stu-id="0745d-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="0745d-112">OS</span><span class="sxs-lookup"><span data-stu-id="0745d-112">PARAMETERS</span></span>

### <span data-ttu-id="0745d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0745d-113">-AsJob</span></span>
<span data-ttu-id="0745d-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0745d-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0745d-115">-DefaultProfile</span></span>
<span data-ttu-id="0745d-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0745d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0745d-117">-Force</span></span>
<span data-ttu-id="0745d-118">Remover o cluster gerenciado kubernetes sem perguntar</span><span class="sxs-lookup"><span data-stu-id="0745d-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0745d-119">-Id</span></span>
<span data-ttu-id="0745d-120">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="0745d-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0745d-121">-InputObject</span></span>
<span data-ttu-id="0745d-122">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="0745d-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="0745d-123">-Name</span></span>
<span data-ttu-id="0745d-124">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="0745d-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0745d-125">-PassThru</span></span>
<span data-ttu-id="0745d-126">Retorna verdadeiro se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="0745d-126">Returns true if deletion is successful</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0745d-127">-ResourceGroupName</span></span>
<span data-ttu-id="0745d-128">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0745d-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0745d-129">-Confirm</span></span>
<span data-ttu-id="0745d-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0745d-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0745d-131">-WhatIf</span></span>
<span data-ttu-id="0745d-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0745d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0745d-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0745d-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0745d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0745d-134">CommonParameters</span></span>
<span data-ttu-id="0745d-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0745d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0745d-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0745d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0745d-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0745d-137">INPUTS</span></span>

### <span data-ttu-id="0745d-138">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="0745d-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="0745d-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0745d-139">System.String</span></span>

## <span data-ttu-id="0745d-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0745d-140">OUTPUTS</span></span>

### <span data-ttu-id="0745d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0745d-141">System.Boolean</span></span>

## <span data-ttu-id="0745d-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0745d-142">NOTES</span></span>

## <span data-ttu-id="0745d-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0745d-143">RELATED LINKS</span></span>
