---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93595746"
---
# <span data-ttu-id="e25e7-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="e25e7-101">New-AzAks</span></span>

## <span data-ttu-id="e25e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e25e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e25e7-103">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e25e7-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e25e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e25e7-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e25e7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e25e7-105">DESCRIPTION</span></span>

<span data-ttu-id="e25e7-106">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e25e7-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e25e7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e25e7-107">EXAMPLES</span></span>

### <span data-ttu-id="e25e7-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e25e7-108">Example 1</span></span>

<span data-ttu-id="e25e7-109">Crie um novo cluster gerenciado kubernetes com parâmetros padrão.</span><span class="sxs-lookup"><span data-stu-id="e25e7-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e25e7-110">OS</span><span class="sxs-lookup"><span data-stu-id="e25e7-110">PARAMETERS</span></span>

### <span data-ttu-id="e25e7-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="e25e7-111">-AdminUserName</span></span>
<span data-ttu-id="e25e7-112">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="e25e7-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="e25e7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e25e7-113">-AsJob</span></span>
<span data-ttu-id="e25e7-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e25e7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e25e7-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="e25e7-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="e25e7-116">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="e25e7-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="e25e7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e25e7-117">-DefaultProfile</span></span>
<span data-ttu-id="e25e7-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e25e7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e25e7-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="e25e7-119">-DnsNamePrefix</span></span>
<span data-ttu-id="e25e7-120">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="e25e7-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="e25e7-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e25e7-121">-Force</span></span>
<span data-ttu-id="e25e7-122">Criar cluster mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="e25e7-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="e25e7-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="e25e7-123">-KubernetesVersion</span></span>
<span data-ttu-id="e25e7-124">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="e25e7-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="e25e7-125">-Local</span><span class="sxs-lookup"><span data-stu-id="e25e7-125">-Location</span></span>
<span data-ttu-id="e25e7-126">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="e25e7-126">Azure location for the cluster.</span></span>
<span data-ttu-id="e25e7-127">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e25e7-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="e25e7-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="e25e7-128">-Name</span></span>
<span data-ttu-id="e25e7-129">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="e25e7-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="e25e7-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="e25e7-130">-NodeCount</span></span>
<span data-ttu-id="e25e7-131">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="e25e7-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="e25e7-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="e25e7-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="e25e7-133">Tamanho em GB do disco do sistema operacional para cada nó no pool de nós.</span><span class="sxs-lookup"><span data-stu-id="e25e7-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="e25e7-134">Mínimo de 30 GB.</span><span class="sxs-lookup"><span data-stu-id="e25e7-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="e25e7-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="e25e7-135">-NodeVmSize</span></span>
<span data-ttu-id="e25e7-136">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e25e7-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="e25e7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e25e7-137">-ResourceGroupName</span></span>
<span data-ttu-id="e25e7-138">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e25e7-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="e25e7-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="e25e7-139">-SshKeyValue</span></span>
<span data-ttu-id="e25e7-140">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="e25e7-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="e25e7-141">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="e25e7-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="e25e7-142">-Marca</span><span class="sxs-lookup"><span data-stu-id="e25e7-142">-Tag</span></span>
<span data-ttu-id="e25e7-143">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="e25e7-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="e25e7-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e25e7-144">-Confirm</span></span>
<span data-ttu-id="e25e7-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e25e7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e25e7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e25e7-146">-WhatIf</span></span>
<span data-ttu-id="e25e7-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e25e7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e25e7-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e25e7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e25e7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e25e7-149">CommonParameters</span></span>
<span data-ttu-id="e25e7-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e25e7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e25e7-151">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e25e7-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e25e7-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e25e7-152">INPUTS</span></span>

### <span data-ttu-id="e25e7-153">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="e25e7-153">None</span></span>

## <span data-ttu-id="e25e7-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e25e7-154">OUTPUTS</span></span>

### <span data-ttu-id="e25e7-155">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e25e7-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="e25e7-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e25e7-156">NOTES</span></span>

## <span data-ttu-id="e25e7-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e25e7-157">RELATED LINKS</span></span>
