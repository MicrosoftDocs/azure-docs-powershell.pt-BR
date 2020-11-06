---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610442"
---
# <span data-ttu-id="2ff2d-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="2ff2d-101">New-AzureRmAks</span></span>

## <span data-ttu-id="2ff2d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ff2d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff2d-103">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ff2d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ff2d-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ff2d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ff2d-105">DESCRIPTION</span></span>
<span data-ttu-id="2ff2d-106">Crie um novo cluster gerenciado kubernetes.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="2ff2d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ff2d-107">EXAMPLES</span></span>

### <span data-ttu-id="2ff2d-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2ff2d-108">Example 1</span></span>
<span data-ttu-id="2ff2d-109">Criar um novo cluster gerenciado kubernetes com parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="2ff2d-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="2ff2d-110">OS</span><span class="sxs-lookup"><span data-stu-id="2ff2d-110">PARAMETERS</span></span>

### <span data-ttu-id="2ff2d-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="2ff2d-111">-AdminUserName</span></span>
<span data-ttu-id="2ff2d-112">Nome de usuário para as máquinas virtuais Linux.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2ff2d-113">-AsJob</span></span>
<span data-ttu-id="2ff2d-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2ff2d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2ff2d-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="2ff2d-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="2ff2d-116">A ID do cliente e o segredo do cliente associado à entidade de serviço/aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ff2d-117">-DefaultProfile</span></span>
<span data-ttu-id="2ff2d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ff2d-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="2ff2d-119">-DnsNamePrefix</span></span>
<span data-ttu-id="2ff2d-120">O prefixo do nome DNS para o cluster.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2ff2d-121">-Force</span></span>
<span data-ttu-id="2ff2d-122">Criar cluster mesmo que ele já exista</span><span class="sxs-lookup"><span data-stu-id="2ff2d-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="2ff2d-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="2ff2d-123">-KubernetesVersion</span></span>
<span data-ttu-id="2ff2d-124">A versão do kubernetes a ser usada para criar o cluster.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-125">-Local</span><span class="sxs-lookup"><span data-stu-id="2ff2d-125">-Location</span></span>
<span data-ttu-id="2ff2d-126">Local do Azure para o cluster.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-126">Azure location for the cluster.</span></span>
<span data-ttu-id="2ff2d-127">O padrão é o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="2ff2d-128">-Name</span></span>
<span data-ttu-id="2ff2d-129">Kubernetes nome do cluster gerenciado.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="2ff2d-130">-NodeCount</span></span>
<span data-ttu-id="2ff2d-131">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="2ff2d-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="2ff2d-133">O número padrão de nós para os pools de nós.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="2ff2d-134">-NodeVmSize</span></span>
<span data-ttu-id="2ff2d-135">O tamanho da máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ff2d-136">-ResourceGroupName</span></span>
<span data-ttu-id="2ff2d-137">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="2ff2d-138">-SshKeyValue</span></span>
<span data-ttu-id="2ff2d-139">Chave do arquivo de chave SSH ou caminho do arquivo de chave.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="2ff2d-140">O padrão é {HOME}/.ssh/id_rsa. pub.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-141">-Marca</span><span class="sxs-lookup"><span data-stu-id="2ff2d-141">-Tag</span></span>
<span data-ttu-id="2ff2d-142">Marcas a serem aplicadas ao recurso</span><span class="sxs-lookup"><span data-stu-id="2ff2d-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff2d-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2ff2d-143">-Confirm</span></span>
<span data-ttu-id="2ff2d-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ff2d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ff2d-145">-WhatIf</span></span>
<span data-ttu-id="2ff2d-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ff2d-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ff2d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff2d-148">CommonParameters</span></span>
<span data-ttu-id="2ff2d-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff2d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff2d-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff2d-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff2d-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ff2d-151">INPUTS</span></span>

### <span data-ttu-id="2ff2d-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2ff2d-152">None</span></span>

## <span data-ttu-id="2ff2d-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ff2d-153">OUTPUTS</span></span>

### <span data-ttu-id="2ff2d-154">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="2ff2d-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="2ff2d-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ff2d-155">NOTES</span></span>

## <span data-ttu-id="2ff2d-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ff2d-156">RELATED LINKS</span></span>
