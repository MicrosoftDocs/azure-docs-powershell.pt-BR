---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAks.md
ms.openlocfilehash: 9b63ede0bbd24adb98159ca6cfee08238b26aabc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598200"
---
# <span data-ttu-id="ffd10-101">Set-AzAks</span><span class="sxs-lookup"><span data-stu-id="ffd10-101">Set-AzAks</span></span>

## <span data-ttu-id="ffd10-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ffd10-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd10-103">Atualize ou crie um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ffd10-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ffd10-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffd10-104">SYNTAX</span></span>

### <span data-ttu-id="ffd10-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ffd10-105">defaultParameterSet (Default)</span></span>
```
Set-AzAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffd10-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffd10-106">InputObjectParameterSet</span></span>
```
Set-AzAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffd10-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffd10-107">IdParameterSet</span></span>
```
Set-AzAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd10-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ffd10-108">DESCRIPTION</span></span>
<span data-ttu-id="ffd10-109">Atualize ou crie um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ffd10-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="ffd10-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffd10-110">EXAMPLES</span></span>

### <span data-ttu-id="ffd10-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ffd10-111">Example 1</span></span>
```
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="ffd10-112">Defina o número de nós no cluster kubernetes para 5.</span><span class="sxs-lookup"><span data-stu-id="ffd10-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="ffd10-113">OS</span><span class="sxs-lookup"><span data-stu-id="ffd10-113">PARAMETERS</span></span>

### <span data-ttu-id="ffd10-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="ffd10-114">-AdminUserName</span></span>
<span data-ttu-id="ffd10-115">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="ffd10-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="ffd10-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffd10-116">-AsJob</span></span>
<span data-ttu-id="ffd10-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ffd10-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ffd10-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="ffd10-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="ffd10-119">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="ffd10-119">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd10-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd10-120">-DefaultProfile</span></span>
<span data-ttu-id="ffd10-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd10-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd10-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="ffd10-122">-DnsNamePrefix</span></span>
<span data-ttu-id="ffd10-123">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="ffd10-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="ffd10-124">-ID</span><span class="sxs-lookup"><span data-stu-id="ffd10-124">-Id</span></span>
<span data-ttu-id="ffd10-125">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="ffd10-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="ffd10-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ffd10-126">-InputObject</span></span>
<span data-ttu-id="ffd10-127">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ffd10-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ffd10-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="ffd10-128">-KubernetesVersion</span></span>
<span data-ttu-id="ffd10-129">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="ffd10-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="ffd10-130">-Local</span><span class="sxs-lookup"><span data-stu-id="ffd10-130">-Location</span></span>
<span data-ttu-id="ffd10-131">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="ffd10-131">Azure location for the cluster.</span></span>
<span data-ttu-id="ffd10-132">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffd10-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="ffd10-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="ffd10-133">-Name</span></span>
<span data-ttu-id="ffd10-134">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="ffd10-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd10-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="ffd10-135">-NodeCount</span></span>
<span data-ttu-id="ffd10-136">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="ffd10-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="ffd10-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="ffd10-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="ffd10-138">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="ffd10-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="ffd10-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="ffd10-139">-NodeVmSize</span></span>
<span data-ttu-id="ffd10-140">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ffd10-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="ffd10-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd10-141">-ResourceGroupName</span></span>
<span data-ttu-id="ffd10-142">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffd10-142">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd10-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="ffd10-143">-SshKeyValue</span></span>
<span data-ttu-id="ffd10-144">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="ffd10-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="ffd10-145">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="ffd10-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="ffd10-146">-Marca</span><span class="sxs-lookup"><span data-stu-id="ffd10-146">-Tag</span></span>
<span data-ttu-id="ffd10-147">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="ffd10-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="ffd10-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ffd10-148">-Confirm</span></span>
<span data-ttu-id="ffd10-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffd10-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd10-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd10-150">-WhatIf</span></span>
<span data-ttu-id="ffd10-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffd10-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd10-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffd10-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd10-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd10-153">CommonParameters</span></span>
<span data-ttu-id="ffd10-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd10-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd10-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd10-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd10-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ffd10-156">INPUTS</span></span>

### <span data-ttu-id="ffd10-157">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ffd10-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="ffd10-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd10-158">System.String</span></span>

## <span data-ttu-id="ffd10-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ffd10-159">OUTPUTS</span></span>

### <span data-ttu-id="ffd10-160">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="ffd10-160">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="ffd10-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ffd10-161">NOTES</span></span>

## <span data-ttu-id="ffd10-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffd10-162">RELATED LINKS</span></span>
