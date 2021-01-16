---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258180"
---
# <span data-ttu-id="c2740-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="c2740-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="c2740-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2740-102">SYNOPSIS</span></span>
<span data-ttu-id="c2740-103">Atualize ou crie um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c2740-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c2740-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2740-104">SYNTAX</span></span>

### <span data-ttu-id="c2740-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2740-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2740-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2740-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2740-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2740-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2740-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2740-108">DESCRIPTION</span></span>
<span data-ttu-id="c2740-109">Atualize ou crie um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c2740-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="c2740-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2740-110">EXAMPLES</span></span>

### <span data-ttu-id="c2740-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c2740-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="c2740-112">Defina o número de nós no cluster kubernetes para 5.</span><span class="sxs-lookup"><span data-stu-id="c2740-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="c2740-113">OS</span><span class="sxs-lookup"><span data-stu-id="c2740-113">PARAMETERS</span></span>

### <span data-ttu-id="c2740-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2740-114">-AsJob</span></span>
<span data-ttu-id="c2740-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c2740-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c2740-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2740-116">-DefaultProfile</span></span>
<span data-ttu-id="c2740-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c2740-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2740-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="c2740-118">-DnsNamePrefix</span></span>
<span data-ttu-id="c2740-119">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="c2740-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="c2740-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="c2740-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="c2740-121">Se o dimensionador automático deve ser habilitado</span><span class="sxs-lookup"><span data-stu-id="c2740-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="c2740-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c2740-122">-Id</span></span>
<span data-ttu-id="c2740-123">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="c2740-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="c2740-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2740-124">-InputObject</span></span>
<span data-ttu-id="c2740-125">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="c2740-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c2740-126">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="c2740-126">-KubernetesVersion</span></span>
<span data-ttu-id="c2740-127">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="c2740-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="c2740-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="c2740-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="c2740-129">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="c2740-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="c2740-130">-Local</span><span class="sxs-lookup"><span data-stu-id="c2740-130">-Location</span></span>
<span data-ttu-id="c2740-131">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="c2740-131">Azure location for the cluster.</span></span>
<span data-ttu-id="c2740-132">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2740-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="c2740-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2740-133">-Name</span></span>
<span data-ttu-id="c2740-134">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c2740-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="c2740-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c2740-135">-NodeCount</span></span>
<span data-ttu-id="c2740-136">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="c2740-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="c2740-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="c2740-137">-NodeMaxCount</span></span>
<span data-ttu-id="c2740-138">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="c2740-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="c2740-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="c2740-139">-NodeMinCount</span></span>
<span data-ttu-id="c2740-140">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="c2740-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="c2740-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c2740-141">-NodeName</span></span>
<span data-ttu-id="c2740-142">Nome exclusivo do perfil do pool do agente no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2740-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="c2740-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="c2740-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="c2740-144">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="c2740-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="c2740-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="c2740-145">-NodePoolMode</span></span>
<span data-ttu-id="c2740-146">NodePoolMode representa o modo de um pool de nós.</span><span class="sxs-lookup"><span data-stu-id="c2740-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="c2740-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="c2740-147">-NodeVmSize</span></span>
<span data-ttu-id="c2740-148">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="c2740-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="c2740-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2740-149">-ResourceGroupName</span></span>
<span data-ttu-id="c2740-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c2740-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2740-151">-ServicePrincipalIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="c2740-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="c2740-152">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="c2740-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="c2740-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="c2740-153">-SshKeyValue</span></span>
<span data-ttu-id="c2740-154">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="c2740-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="c2740-155">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="c2740-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="c2740-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="c2740-156">-Tag</span></span>
<span data-ttu-id="c2740-157">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="c2740-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="c2740-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2740-158">-Confirm</span></span>
<span data-ttu-id="c2740-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2740-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2740-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2740-160">-WhatIf</span></span>
<span data-ttu-id="c2740-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2740-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2740-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2740-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2740-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2740-163">CommonParameters</span></span>
<span data-ttu-id="c2740-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2740-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2740-165">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2740-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2740-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2740-166">INPUTS</span></span>

### <span data-ttu-id="c2740-167">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c2740-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c2740-168">System. String</span><span class="sxs-lookup"><span data-stu-id="c2740-168">System.String</span></span>

## <span data-ttu-id="c2740-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2740-169">OUTPUTS</span></span>

### <span data-ttu-id="c2740-170">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c2740-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c2740-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2740-171">NOTES</span></span>

## <span data-ttu-id="c2740-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2740-172">RELATED LINKS</span></span>
