---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/import-azakscredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Import-AzAksCredential.md
ms.openlocfilehash: fe4e56e809dd2cda7c650e24b55ae3867a23a7b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117114"
---
# <span data-ttu-id="bc4db-101">Import-AzAksCredential</span><span class="sxs-lookup"><span data-stu-id="bc4db-101">Import-AzAksCredential</span></span>

## <span data-ttu-id="bc4db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bc4db-102">SYNOPSIS</span></span>
<span data-ttu-id="bc4db-103">Importar e mesclar a configuração do Kubectl para um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="bc4db-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="bc4db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bc4db-104">SYNTAX</span></span>

### <span data-ttu-id="bc4db-105">GroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bc4db-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc4db-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc4db-106">InputObjectParameterSet</span></span>
```
Import-AzAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc4db-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc4db-107">IdParameterSet</span></span>
```
Import-AzAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc4db-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bc4db-108">DESCRIPTION</span></span>
<span data-ttu-id="bc4db-109">Importar e mesclar a configuração do Kubectl para um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="bc4db-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="bc4db-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bc4db-110">EXAMPLES</span></span>

### <span data-ttu-id="bc4db-111">Importar e mesclar a configuração do Kubectl</span><span class="sxs-lookup"><span data-stu-id="bc4db-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="bc4db-112">OS</span><span class="sxs-lookup"><span data-stu-id="bc4db-112">PARAMETERS</span></span>

### <span data-ttu-id="bc4db-113">-Administrador</span><span class="sxs-lookup"><span data-stu-id="bc4db-113">-Admin</span></span>
<span data-ttu-id="bc4db-114">Obtenha a configuração ' clusterAdmin' kubectl em vez do ' clusterUser ' padrão.</span><span class="sxs-lookup"><span data-stu-id="bc4db-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="bc4db-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="bc4db-115">-ConfigPath</span></span>
<span data-ttu-id="bc4db-116">Um arquivo de configuração kubectl para criar ou atualizar.</span><span class="sxs-lookup"><span data-stu-id="bc4db-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="bc4db-117">Use '-' para imprimir YAML em stdout em vez disso.</span><span class="sxs-lookup"><span data-stu-id="bc4db-117">Use '-' to print YAML to stdout instead.</span></span>
<span data-ttu-id="bc4db-118">Padrão:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="bc4db-118">Default: %Home%/.kube/config.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc4db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc4db-119">-DefaultProfile</span></span>
<span data-ttu-id="bc4db-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bc4db-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc4db-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bc4db-121">-Force</span></span>
<span data-ttu-id="bc4db-122">Importar a configuração do kubernetes mesmo se for o padrão</span><span class="sxs-lookup"><span data-stu-id="bc4db-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="bc4db-123">-ID</span><span class="sxs-lookup"><span data-stu-id="bc4db-123">-Id</span></span>
<span data-ttu-id="bc4db-124">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="bc4db-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="bc4db-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc4db-125">-InputObject</span></span>
<span data-ttu-id="bc4db-126">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="bc4db-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="bc4db-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="bc4db-127">-Name</span></span>
<span data-ttu-id="bc4db-128">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="bc4db-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="bc4db-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc4db-129">-PassThru</span></span>
<span data-ttu-id="bc4db-130">Retorna verdadeiro se a importação for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="bc4db-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="bc4db-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc4db-131">-ResourceGroupName</span></span>
<span data-ttu-id="bc4db-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="bc4db-132">Resource group name</span></span>

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

### <span data-ttu-id="bc4db-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bc4db-133">-Confirm</span></span>
<span data-ttu-id="bc4db-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc4db-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc4db-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc4db-135">-WhatIf</span></span>
<span data-ttu-id="bc4db-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bc4db-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc4db-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bc4db-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc4db-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc4db-138">CommonParameters</span></span>
<span data-ttu-id="bc4db-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc4db-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc4db-140">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc4db-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc4db-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bc4db-141">INPUTS</span></span>

### <span data-ttu-id="bc4db-142">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="bc4db-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="bc4db-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bc4db-143">System.String</span></span>

## <span data-ttu-id="bc4db-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bc4db-144">OUTPUTS</span></span>

### <span data-ttu-id="bc4db-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bc4db-145">System.String</span></span>

## <span data-ttu-id="bc4db-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bc4db-146">NOTES</span></span>

## <span data-ttu-id="bc4db-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bc4db-147">RELATED LINKS</span></span>
