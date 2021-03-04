---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0cf25018ad9cb432b739f5beeb147d20272d7f50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891905"
---
# <span data-ttu-id="abbb8-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="abbb8-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="abbb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abbb8-102">SYNOPSIS</span></span>
<span data-ttu-id="abbb8-103">Atualizar ou criar um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="abbb8-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="abbb8-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="abbb8-104">SYNTAX</span></span>

### <span data-ttu-id="abbb8-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="abbb8-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abbb8-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abbb8-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abbb8-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abbb8-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abbb8-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="abbb8-108">DESCRIPTION</span></span>
<span data-ttu-id="abbb8-109">Atualizar ou criar um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="abbb8-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="abbb8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abbb8-110">EXAMPLES</span></span>

### <span data-ttu-id="abbb8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="abbb8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="abbb8-112">De definir o número de nós no cluster Kubernetes como 5.</span><span class="sxs-lookup"><span data-stu-id="abbb8-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="abbb8-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="abbb8-113">PARAMETERS</span></span>

### <span data-ttu-id="abbb8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="abbb8-114">-AsJob</span></span>
<span data-ttu-id="abbb8-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="abbb8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="abbb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbb8-116">-DefaultProfile</span></span>
<span data-ttu-id="abbb8-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="abbb8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abbb8-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="abbb8-118">-DnsNamePrefix</span></span>
<span data-ttu-id="abbb8-119">O prefixo de nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="abbb8-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="abbb8-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="abbb8-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="abbb8-121">Se deve habilitar o dimensionador automático</span><span class="sxs-lookup"><span data-stu-id="abbb8-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="abbb8-122">-Id</span><span class="sxs-lookup"><span data-stu-id="abbb8-122">-Id</span></span>
<span data-ttu-id="abbb8-123">ID de um cluster kubernetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="abbb8-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="abbb8-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abbb8-124">-InputObject</span></span>
<span data-ttu-id="abbb8-125">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="abbb8-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="abbb8-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="abbb8-126">-KubernetesVersion</span></span>
<span data-ttu-id="abbb8-127">A versão do Kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="abbb8-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="abbb8-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="abbb8-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="abbb8-129">Nome de usuário para as Máquinas Virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="abbb8-129">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AdminUserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abbb8-130">-Location</span><span class="sxs-lookup"><span data-stu-id="abbb8-130">-Location</span></span>
<span data-ttu-id="abbb8-131">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="abbb8-131">Azure location for the cluster.</span></span>
<span data-ttu-id="abbb8-132">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="abbb8-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="abbb8-133">-Name</span><span class="sxs-lookup"><span data-stu-id="abbb8-133">-Name</span></span>
<span data-ttu-id="abbb8-134">Nome do cluster gerenciado do Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="abbb8-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="abbb8-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="abbb8-135">-NodeCount</span></span>
<span data-ttu-id="abbb8-136">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="abbb8-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="abbb8-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="abbb8-137">-NodeMaxCount</span></span>
<span data-ttu-id="abbb8-138">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="abbb8-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="abbb8-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="abbb8-139">-NodeMinCount</span></span>
<span data-ttu-id="abbb8-140">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="abbb8-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="abbb8-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="abbb8-141">-NodeName</span></span>
<span data-ttu-id="abbb8-142">Nome exclusivo do perfil do pool de agentes no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="abbb8-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="abbb8-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="abbb8-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="abbb8-144">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="abbb8-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="abbb8-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="abbb8-145">-NodePoolMode</span></span>
<span data-ttu-id="abbb8-146">NodePoolMode representa o modo de um pool de nós.</span><span class="sxs-lookup"><span data-stu-id="abbb8-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="abbb8-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="abbb8-147">-NodeVmSize</span></span>
<span data-ttu-id="abbb8-148">O tamanho da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="abbb8-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="abbb8-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abbb8-149">-ResourceGroupName</span></span>
<span data-ttu-id="abbb8-150">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="abbb8-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="abbb8-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="abbb8-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="abbb8-152">A ID do cliente e o segredo do cliente associados à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="abbb8-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="abbb8-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="abbb8-153">-SshKeyValue</span></span>
<span data-ttu-id="abbb8-154">Valor do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="abbb8-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="abbb8-155">O padrão é {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="abbb8-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="abbb8-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="abbb8-156">-Tag</span></span>
<span data-ttu-id="abbb8-157">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="abbb8-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="abbb8-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="abbb8-158">-Confirm</span></span>
<span data-ttu-id="abbb8-159">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abbb8-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abbb8-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abbb8-160">-WhatIf</span></span>
<span data-ttu-id="abbb8-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abbb8-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abbb8-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abbb8-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abbb8-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbb8-163">CommonParameters</span></span>
<span data-ttu-id="abbb8-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abbb8-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abbb8-165">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="abbb8-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbb8-166">INPUTS</span><span class="sxs-lookup"><span data-stu-id="abbb8-166">INPUTS</span></span>

### <span data-ttu-id="abbb8-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="abbb8-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="abbb8-168">System.String</span><span class="sxs-lookup"><span data-stu-id="abbb8-168">System.String</span></span>

## <span data-ttu-id="abbb8-169">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="abbb8-169">OUTPUTS</span></span>

### <span data-ttu-id="abbb8-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="abbb8-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="abbb8-171">NOTES</span><span class="sxs-lookup"><span data-stu-id="abbb8-171">NOTES</span></span>

## <span data-ttu-id="abbb8-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abbb8-172">RELATED LINKS</span></span>
