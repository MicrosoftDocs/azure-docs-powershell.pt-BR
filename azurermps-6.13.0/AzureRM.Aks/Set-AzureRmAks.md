---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/set-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
ms.openlocfilehash: b5d3248c81507abf6092aa4354691975c4b4bc13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428670"
---
# <span data-ttu-id="7d6b0-101">Set-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="7d6b0-101">Set-AzureRmAks</span></span>

## <span data-ttu-id="7d6b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d6b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6b0-103">Atualize ou crie um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-103">Update or create a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d6b0-104">SYNTAX</span></span>

### <span data-ttu-id="7d6b0-105">DefaultParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="7d6b0-105">defaultParameterSet (Default)</span></span>
```
Set-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6b0-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d6b0-106">InputObjectParameterSet</span></span>
```
Set-AzureRmAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6b0-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d6b0-107">IdParameterSet</span></span>
```
Set-AzureRmAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6b0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d6b0-108">DESCRIPTION</span></span>
<span data-ttu-id="7d6b0-109">Atualize ou crie um cluster do kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="7d6b0-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d6b0-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6b0-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7d6b0-111">Example 1</span></span>
```
PS C:\> Get-AzureRmAks -ResourceGroupName group -Name myCluster | Set-AzureRmAks -NodeCount 5
```

<span data-ttu-id="7d6b0-112">Defina o número de nós no cluster kubernetes para 5.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="7d6b0-113">OS</span><span class="sxs-lookup"><span data-stu-id="7d6b0-113">PARAMETERS</span></span>

### <span data-ttu-id="7d6b0-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="7d6b0-114">-AdminUserName</span></span>
<span data-ttu-id="7d6b0-115">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="7d6b0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d6b0-116">-AsJob</span></span>
<span data-ttu-id="7d6b0-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7d6b0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d6b0-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="7d6b0-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="7d6b0-119">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-119">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="7d6b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6b0-120">-DefaultProfile</span></span>
<span data-ttu-id="7d6b0-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6b0-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="7d6b0-122">-DnsNamePrefix</span></span>
<span data-ttu-id="7d6b0-123">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="7d6b0-124">-ID</span><span class="sxs-lookup"><span data-stu-id="7d6b0-124">-Id</span></span>
<span data-ttu-id="7d6b0-125">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="7d6b0-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="7d6b0-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d6b0-126">-InputObject</span></span>
<span data-ttu-id="7d6b0-127">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="7d6b0-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="7d6b0-128">-KubernetesVersion</span></span>
<span data-ttu-id="7d6b0-129">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="7d6b0-130">-Local</span><span class="sxs-lookup"><span data-stu-id="7d6b0-130">-Location</span></span>
<span data-ttu-id="7d6b0-131">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-131">Azure location for the cluster.</span></span>
<span data-ttu-id="7d6b0-132">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="7d6b0-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d6b0-133">-Name</span></span>
<span data-ttu-id="7d6b0-134">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-134">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="7d6b0-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="7d6b0-135">-NodeCount</span></span>
<span data-ttu-id="7d6b0-136">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-136">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="7d6b0-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="7d6b0-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="7d6b0-138">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-138">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="7d6b0-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="7d6b0-139">-NodeVmSize</span></span>
<span data-ttu-id="7d6b0-140">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="7d6b0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6b0-141">-ResourceGroupName</span></span>
<span data-ttu-id="7d6b0-142">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-142">Resource Group Name.</span></span>

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

### <span data-ttu-id="7d6b0-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="7d6b0-143">-SshKeyValue</span></span>
<span data-ttu-id="7d6b0-144">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="7d6b0-145">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="7d6b0-146">-Marca</span><span class="sxs-lookup"><span data-stu-id="7d6b0-146">-Tag</span></span>
<span data-ttu-id="7d6b0-147">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="7d6b0-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="7d6b0-148">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d6b0-148">-Confirm</span></span>
<span data-ttu-id="7d6b0-149">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6b0-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6b0-150">-WhatIf</span></span>
<span data-ttu-id="7d6b0-151">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6b0-152">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6b0-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6b0-153">CommonParameters</span></span>
<span data-ttu-id="7d6b0-154">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d6b0-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6b0-155">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6b0-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6b0-156">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d6b0-156">INPUTS</span></span>

### <span data-ttu-id="7d6b0-157">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7d6b0-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="7d6b0-158">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d6b0-158">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="7d6b0-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7d6b0-159">System.String</span></span>

## <span data-ttu-id="7d6b0-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d6b0-160">OUTPUTS</span></span>

### <span data-ttu-id="7d6b0-161">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="7d6b0-161">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="7d6b0-162">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d6b0-162">NOTES</span></span>

## <span data-ttu-id="7d6b0-163">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d6b0-163">RELATED LINKS</span></span>
