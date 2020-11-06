---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: 31170e24e88f6ce25c9fd344d254189eeeae64f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602744"
---
# <span data-ttu-id="85420-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85420-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="85420-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85420-102">SYNOPSIS</span></span>
<span data-ttu-id="85420-103">Cria uma replicação de registro de contêiner.</span><span class="sxs-lookup"><span data-stu-id="85420-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85420-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85420-104">SYNTAX</span></span>

### <span data-ttu-id="85420-105">NameResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="85420-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85420-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85420-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85420-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85420-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85420-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85420-108">DESCRIPTION</span></span>
<span data-ttu-id="85420-109">O cmdlet New-AzureRmContainerRegistryReplication cria uma nova replicação de registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="85420-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="85420-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85420-110">EXAMPLES</span></span>

### <span data-ttu-id="85420-111">Exemplo 1: criar uma nova replicação de registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="85420-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="85420-112">Crie uma nova replicação de registro de contêineres.</span><span class="sxs-lookup"><span data-stu-id="85420-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="85420-113">OS</span><span class="sxs-lookup"><span data-stu-id="85420-113">PARAMETERS</span></span>

### <span data-ttu-id="85420-114">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85420-114">-Confirm</span></span>
<span data-ttu-id="85420-115">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85420-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85420-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85420-116">-DefaultProfile</span></span>
<span data-ttu-id="85420-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="85420-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85420-118">-Local</span><span class="sxs-lookup"><span data-stu-id="85420-118">-Location</span></span>
<span data-ttu-id="85420-119">Local do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="85420-119">Container Registry Location.</span></span>
<span data-ttu-id="85420-120">Padrão para o local do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85420-120">Default to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85420-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="85420-121">-Name</span></span>
<span data-ttu-id="85420-122">Nome de replicação do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="85420-122">Container Registry Replication Name.</span></span>
<span data-ttu-id="85420-123">Padrão para o nome do local.</span><span class="sxs-lookup"><span data-stu-id="85420-123">Default to the location name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85420-124">-Registro</span><span class="sxs-lookup"><span data-stu-id="85420-124">-Registry</span></span>
<span data-ttu-id="85420-125">Objeto do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="85420-125">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85420-126">-Registryname</span><span class="sxs-lookup"><span data-stu-id="85420-126">-RegistryName</span></span>
<span data-ttu-id="85420-127">Nome do registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="85420-127">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85420-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85420-128">-ResourceGroupName</span></span>
<span data-ttu-id="85420-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="85420-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85420-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85420-130">-ResourceId</span></span>
<span data-ttu-id="85420-131">A ID do recurso do registro do contêiner</span><span class="sxs-lookup"><span data-stu-id="85420-131">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85420-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="85420-132">-Tag</span></span>
<span data-ttu-id="85420-133">Marcas de registro do contêiner.</span><span class="sxs-lookup"><span data-stu-id="85420-133">Container Registry Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85420-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85420-134">-WhatIf</span></span>
<span data-ttu-id="85420-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85420-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85420-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85420-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85420-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85420-137">CommonParameters</span></span>
<span data-ttu-id="85420-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85420-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85420-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85420-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85420-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85420-140">INPUTS</span></span>

### <span data-ttu-id="85420-141">System. String</span><span class="sxs-lookup"><span data-stu-id="85420-141">System.String</span></span>

## <span data-ttu-id="85420-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85420-142">OUTPUTS</span></span>

### <span data-ttu-id="85420-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85420-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="85420-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85420-144">NOTES</span></span>

## <span data-ttu-id="85420-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85420-145">RELATED LINKS</span></span>

[<span data-ttu-id="85420-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85420-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="85420-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="85420-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
