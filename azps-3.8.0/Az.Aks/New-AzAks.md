---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: a5a376fea0dc40bbfd02ea1cb430c725c2bc14e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943885"
---
# <span data-ttu-id="fb533-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="fb533-101">New-AzAks</span></span>

## <span data-ttu-id="fb533-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb533-102">SYNOPSIS</span></span>
<span data-ttu-id="fb533-103">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fb533-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="fb533-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb533-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb533-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb533-105">DESCRIPTION</span></span>

<span data-ttu-id="fb533-106">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fb533-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="fb533-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb533-107">EXAMPLES</span></span>

### <span data-ttu-id="fb533-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fb533-108">Example 1</span></span>

<span data-ttu-id="fb533-109">Crie um novo cluster gerenciado kubernetes com parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="fb533-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="fb533-110">OS</span><span class="sxs-lookup"><span data-stu-id="fb533-110">PARAMETERS</span></span>

### <span data-ttu-id="fb533-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="fb533-111">-AdminUserName</span></span>
<span data-ttu-id="fb533-112">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="fb533-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="fb533-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fb533-113">-AsJob</span></span>
<span data-ttu-id="fb533-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="fb533-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fb533-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="fb533-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="fb533-116">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="fb533-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb533-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb533-117">-DefaultProfile</span></span>
<span data-ttu-id="fb533-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb533-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb533-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="fb533-119">-DnsNamePrefix</span></span>
<span data-ttu-id="fb533-120">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="fb533-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="fb533-121">-Force</span><span class="sxs-lookup"><span data-stu-id="fb533-121">-Force</span></span>
<span data-ttu-id="fb533-122">Criar cluster mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="fb533-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="fb533-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="fb533-123">-KubernetesVersion</span></span>
<span data-ttu-id="fb533-124">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="fb533-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="fb533-125">-Local</span><span class="sxs-lookup"><span data-stu-id="fb533-125">-Location</span></span>
<span data-ttu-id="fb533-126">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="fb533-126">Azure location for the cluster.</span></span>
<span data-ttu-id="fb533-127">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb533-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="fb533-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb533-128">-Name</span></span>
<span data-ttu-id="fb533-129">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="fb533-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="fb533-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="fb533-130">-NodeCount</span></span>
<span data-ttu-id="fb533-131">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="fb533-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb533-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="fb533-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="fb533-133">Tamanho em GB do disco do sistema operacional para cada nó no pool de nós.</span><span class="sxs-lookup"><span data-stu-id="fb533-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="fb533-134">Mínimo de 30 GB.</span><span class="sxs-lookup"><span data-stu-id="fb533-134">Minimum 30 GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb533-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="fb533-135">-NodeVmSize</span></span>
<span data-ttu-id="fb533-136">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="fb533-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="fb533-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb533-137">-ResourceGroupName</span></span>
<span data-ttu-id="fb533-138">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fb533-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb533-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="fb533-139">-SshKeyValue</span></span>
<span data-ttu-id="fb533-140">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="fb533-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="fb533-141">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="fb533-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb533-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="fb533-142">-Tag</span></span>
<span data-ttu-id="fb533-143">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="fb533-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="fb533-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb533-144">-Confirm</span></span>
<span data-ttu-id="fb533-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb533-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb533-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb533-146">-WhatIf</span></span>
<span data-ttu-id="fb533-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb533-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb533-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb533-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb533-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb533-149">CommonParameters</span></span>
<span data-ttu-id="fb533-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb533-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb533-151">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb533-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb533-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb533-152">INPUTS</span></span>

### <span data-ttu-id="fb533-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="fb533-153">None</span></span>

## <span data-ttu-id="fb533-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb533-154">OUTPUTS</span></span>

### <span data-ttu-id="fb533-155">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fb533-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="fb533-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb533-156">NOTES</span></span>

## <span data-ttu-id="fb533-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb533-157">RELATED LINKS</span></span>
