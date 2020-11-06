---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/import-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Import-AzureRmAksCredential.md
ms.openlocfilehash: 9a95f6a6b299114c52e011c3a1abdc6fa8651c81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426852"
---
# <span data-ttu-id="87eed-101">Import-AzureRmAksCredential</span><span class="sxs-lookup"><span data-stu-id="87eed-101">Import-AzureRmAksCredential</span></span>

## <span data-ttu-id="87eed-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87eed-102">SYNOPSIS</span></span>
<span data-ttu-id="87eed-103">Importar e mesclar a configuração do Kubectl para um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="87eed-103">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87eed-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87eed-104">SYNTAX</span></span>

### <span data-ttu-id="87eed-105">GroupNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="87eed-105">GroupNameParameterSet (Default)</span></span>
```
Import-AzureRmAksCredential [-ResourceGroupName] <String> [-Name] <String> [-Admin] [-ConfigPath <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87eed-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87eed-106">InputObjectParameterSet</span></span>
```
Import-AzureRmAksCredential -InputObject <PSKubernetesCluster> [-Admin] [-ConfigPath <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87eed-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87eed-107">IdParameterSet</span></span>
```
Import-AzureRmAksCredential [-Id] <String> [-Admin] [-ConfigPath <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87eed-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87eed-108">DESCRIPTION</span></span>
<span data-ttu-id="87eed-109">Importar e mesclar a configuração do Kubectl para um cluster kubernetes gerenciado.</span><span class="sxs-lookup"><span data-stu-id="87eed-109">Import and merge Kubectl config for a managed Kubernetes Cluster.</span></span>

## <span data-ttu-id="87eed-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87eed-110">EXAMPLES</span></span>

### <span data-ttu-id="87eed-111">Importar e mesclar a configuração do Kubectl</span><span class="sxs-lookup"><span data-stu-id="87eed-111">Import and merge Kubectl config</span></span>
```
PS C:\> Import-AzureRmAksCredential -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="87eed-112">OS</span><span class="sxs-lookup"><span data-stu-id="87eed-112">PARAMETERS</span></span>

### <span data-ttu-id="87eed-113">-Administrador</span><span class="sxs-lookup"><span data-stu-id="87eed-113">-Admin</span></span>
<span data-ttu-id="87eed-114">Obtenha a configuração ' clusterAdmin' kubectl em vez do ' clusterUser ' padrão.</span><span class="sxs-lookup"><span data-stu-id="87eed-114">Get the 'clusterAdmin' kubectl config instead of the default 'clusterUser'.</span></span>

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

### <span data-ttu-id="87eed-115">-ConfigPath</span><span class="sxs-lookup"><span data-stu-id="87eed-115">-ConfigPath</span></span>
<span data-ttu-id="87eed-116">Um arquivo de configuração kubectl para criar ou atualizar.</span><span class="sxs-lookup"><span data-stu-id="87eed-116">A kubectl config file to create or update.</span></span>
<span data-ttu-id="87eed-117">Use '-' para imprimir YAML em stdout em vez disso.</span><span class="sxs-lookup"><span data-stu-id="87eed-117">Use '-' to print YAML to stdout instead.</span></span> <span data-ttu-id="87eed-118">Padrão:% Home%/.Kube/config.</span><span class="sxs-lookup"><span data-stu-id="87eed-118">Default: %Home%/.kube/config.</span></span>

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

### <span data-ttu-id="87eed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87eed-119">-DefaultProfile</span></span>
<span data-ttu-id="87eed-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87eed-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87eed-121">-Force</span><span class="sxs-lookup"><span data-stu-id="87eed-121">-Force</span></span>
<span data-ttu-id="87eed-122">Importar a configuração do kubernetes mesmo se for o padrão</span><span class="sxs-lookup"><span data-stu-id="87eed-122">Import Kubernetes config even if it is the default</span></span>

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

### <span data-ttu-id="87eed-123">-ID</span><span class="sxs-lookup"><span data-stu-id="87eed-123">-Id</span></span>
<span data-ttu-id="87eed-124">ID de um cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="87eed-124">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="87eed-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87eed-125">-InputObject</span></span>
<span data-ttu-id="87eed-126">Um objeto PSKubernetesCluster, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="87eed-126">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="87eed-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="87eed-127">-Name</span></span>
<span data-ttu-id="87eed-128">Nome do seu cluster gerenciado do kubernetes</span><span class="sxs-lookup"><span data-stu-id="87eed-128">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="87eed-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87eed-129">-PassThru</span></span>
<span data-ttu-id="87eed-130">Retorna verdadeiro se a importação for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="87eed-130">Returns true if import is successful</span></span>

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

### <span data-ttu-id="87eed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87eed-131">-ResourceGroupName</span></span>
<span data-ttu-id="87eed-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="87eed-132">Resource group name</span></span>

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

### <span data-ttu-id="87eed-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="87eed-133">-Confirm</span></span>
<span data-ttu-id="87eed-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87eed-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87eed-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87eed-135">-WhatIf</span></span>
<span data-ttu-id="87eed-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="87eed-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87eed-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="87eed-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87eed-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87eed-138">CommonParameters</span></span>
<span data-ttu-id="87eed-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87eed-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87eed-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87eed-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87eed-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87eed-141">INPUTS</span></span>

### <span data-ttu-id="87eed-142">Microsoft. Azure. Commands. AKs. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="87eed-142">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="87eed-143">System. String</span><span class="sxs-lookup"><span data-stu-id="87eed-143">System.String</span></span>

## <span data-ttu-id="87eed-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87eed-144">OUTPUTS</span></span>

### <span data-ttu-id="87eed-145">System. String</span><span class="sxs-lookup"><span data-stu-id="87eed-145">System.String</span></span>

## <span data-ttu-id="87eed-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87eed-146">NOTES</span></span>

## <span data-ttu-id="87eed-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87eed-147">RELATED LINKS</span></span>
