---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/set-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Set-AzAksCluster.md
ms.openlocfilehash: 0df5c0d9975acc048ba5842543ec2c4d522567c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118112"
---
# <span data-ttu-id="a6a91-101">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="a6a91-101">Set-AzAksCluster</span></span>

## <span data-ttu-id="a6a91-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6a91-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a91-103">Atualize ou crie um cluster Desavendas gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a6a91-103">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a6a91-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6a91-104">SYNTAX</span></span>

### <span data-ttu-id="a6a91-105">defaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a6a91-105">defaultParameterSet (Default)</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-ServicePrincipalIdAndSecret] <PSCredential>] [-Location <String>] [-LinuxProfileAdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeName <String>] [-NodeMinCount <Int32>]
 [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a91-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a91-106">InputObjectParameterSet</span></span>
```
Set-AzAksCluster -InputObject <PSKubernetesCluster> [-NodePoolMode <String>] [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a91-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a91-107">IdParameterSet</span></span>
```
Set-AzAksCluster [-NodePoolMode <String>] [-Id] <String> [-Location <String>]
 [-LinuxProfileAdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeName <String>] [-NodeMinCount <Int32>] [-NodeMaxCount <Int32>] [-EnableNodeAutoScaling]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a91-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a6a91-108">DESCRIPTION</span></span>
<span data-ttu-id="a6a91-109">Atualize ou crie um cluster Desavendas gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a6a91-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="a6a91-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6a91-110">EXAMPLES</span></span>

### <span data-ttu-id="a6a91-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a6a91-111">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Set-AzAks -NodeCount 5
```

<span data-ttu-id="a6a91-112">De definir o número de nós no cluster Desernetes como 5.</span><span class="sxs-lookup"><span data-stu-id="a6a91-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="a6a91-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6a91-113">PARAMETERS</span></span>

### <span data-ttu-id="a6a91-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6a91-114">-AsJob</span></span>
<span data-ttu-id="a6a91-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a6a91-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a6a91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a91-116">-DefaultProfile</span></span>
<span data-ttu-id="a6a91-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a91-118">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="a6a91-118">-DnsNamePrefix</span></span>
<span data-ttu-id="a6a91-119">O prefixo de nome DNS do cluster.</span><span class="sxs-lookup"><span data-stu-id="a6a91-119">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="a6a91-120">-EnableNodeAutoScaling</span><span class="sxs-lookup"><span data-stu-id="a6a91-120">-EnableNodeAutoScaling</span></span>
<span data-ttu-id="a6a91-121">Se você quer habilitar o dimensionador automático</span><span class="sxs-lookup"><span data-stu-id="a6a91-121">Whether to enable auto-scaler</span></span>

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

### <span data-ttu-id="a6a91-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a6a91-122">-Id</span></span>
<span data-ttu-id="a6a91-123">ID de um cluster de Redenetes gerenciado</span><span class="sxs-lookup"><span data-stu-id="a6a91-123">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="a6a91-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6a91-124">-InputObject</span></span>
<span data-ttu-id="a6a91-125">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a6a91-125">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="a6a91-126">-LtdernetesVersion</span><span class="sxs-lookup"><span data-stu-id="a6a91-126">-KubernetesVersion</span></span>
<span data-ttu-id="a6a91-127">A versão do Queernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="a6a91-127">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="a6a91-128">-LinuxProfileAdminUserName</span><span class="sxs-lookup"><span data-stu-id="a6a91-128">-LinuxProfileAdminUserName</span></span>
<span data-ttu-id="a6a91-129">Nome de usuário para as Máquinas Virtuais do Linux.</span><span class="sxs-lookup"><span data-stu-id="a6a91-129">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="a6a91-130">-Local</span><span class="sxs-lookup"><span data-stu-id="a6a91-130">-Location</span></span>
<span data-ttu-id="a6a91-131">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="a6a91-131">Azure location for the cluster.</span></span>
<span data-ttu-id="a6a91-132">Padrões para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6a91-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="a6a91-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6a91-133">-Name</span></span>
<span data-ttu-id="a6a91-134">Nome de cluster gerenciado por RedeNetes.</span><span class="sxs-lookup"><span data-stu-id="a6a91-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="a6a91-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="a6a91-135">-NodeCount</span></span>
<span data-ttu-id="a6a91-136">O número padrão de nós para os pools de nó.</span><span class="sxs-lookup"><span data-stu-id="a6a91-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="a6a91-137">-NodeMaxCount</span><span class="sxs-lookup"><span data-stu-id="a6a91-137">-NodeMaxCount</span></span>
<span data-ttu-id="a6a91-138">Número máximo de nós para dimensionamento automático</span><span class="sxs-lookup"><span data-stu-id="a6a91-138">Maximum number of nodes for auto-scaling</span></span>

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

### <span data-ttu-id="a6a91-139">-NodeMinCount</span><span class="sxs-lookup"><span data-stu-id="a6a91-139">-NodeMinCount</span></span>
<span data-ttu-id="a6a91-140">Número mínimo de nós para dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="a6a91-140">Minimum number of nodes for auto-scaling.</span></span>

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

### <span data-ttu-id="a6a91-141">-NodeName</span><span class="sxs-lookup"><span data-stu-id="a6a91-141">-NodeName</span></span>
<span data-ttu-id="a6a91-142">Nome exclusivo do perfil de pool do agente no contexto da assinatura e do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6a91-142">Unique name of the agent pool profile in the context of the subscription and resource group.</span></span>

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

### <span data-ttu-id="a6a91-143">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="a6a91-143">-NodeOsDiskSize</span></span>
<span data-ttu-id="a6a91-144">O número padrão de nós para os pools de nó.</span><span class="sxs-lookup"><span data-stu-id="a6a91-144">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="a6a91-145">-NodePoolMode</span><span class="sxs-lookup"><span data-stu-id="a6a91-145">-NodePoolMode</span></span>
<span data-ttu-id="a6a91-146">NodePoolMode representa o modo de um pool de nó.</span><span class="sxs-lookup"><span data-stu-id="a6a91-146">NodePoolMode represents mode of an node pool.</span></span>

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

### <span data-ttu-id="a6a91-147">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="a6a91-147">-NodeVmSize</span></span>
<span data-ttu-id="a6a91-148">O tamanho da Máquina Virtual.</span><span class="sxs-lookup"><span data-stu-id="a6a91-148">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="a6a91-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a91-149">-ResourceGroupName</span></span>
<span data-ttu-id="a6a91-150">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="a6a91-150">Resource Group Name.</span></span>

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

### <span data-ttu-id="a6a91-151">-ServicePrincipalIdAndSecsecsec</span><span class="sxs-lookup"><span data-stu-id="a6a91-151">-ServicePrincipalIdAndSecret</span></span>
<span data-ttu-id="a6a91-152">A ID do cliente e o segredo do cliente associados à entidade de serviço/aplicativo do AAD.</span><span class="sxs-lookup"><span data-stu-id="a6a91-152">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="a6a91-153">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="a6a91-153">-SshKeyValue</span></span>
<span data-ttu-id="a6a91-154">O valor de arquivo da chave SSH ou o caminho do arquivo-chave.</span><span class="sxs-lookup"><span data-stu-id="a6a91-154">SSH key file value or key file path.</span></span>
<span data-ttu-id="a6a91-155">Padrões para {HOME}/.ssh/id_rsa.pub.</span><span class="sxs-lookup"><span data-stu-id="a6a91-155">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="a6a91-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6a91-156">-Tag</span></span>
<span data-ttu-id="a6a91-157">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="a6a91-157">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="a6a91-158">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a6a91-158">-Confirm</span></span>
<span data-ttu-id="a6a91-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6a91-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6a91-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a91-160">-WhatIf</span></span>
<span data-ttu-id="a6a91-161">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a6a91-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a91-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6a91-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6a91-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a91-163">CommonParameters</span></span>
<span data-ttu-id="a6a91-164">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a91-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a91-165">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6a91-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a91-166">Entradas</span><span class="sxs-lookup"><span data-stu-id="a6a91-166">INPUTS</span></span>

### <span data-ttu-id="a6a91-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a6a91-167">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="a6a91-168">System.String</span><span class="sxs-lookup"><span data-stu-id="a6a91-168">System.String</span></span>

## <span data-ttu-id="a6a91-169">Saídas</span><span class="sxs-lookup"><span data-stu-id="a6a91-169">OUTPUTS</span></span>

### <span data-ttu-id="a6a91-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="a6a91-170">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="a6a91-171">Notas</span><span class="sxs-lookup"><span data-stu-id="a6a91-171">NOTES</span></span>

## <span data-ttu-id="a6a91-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6a91-172">RELATED LINKS</span></span>
