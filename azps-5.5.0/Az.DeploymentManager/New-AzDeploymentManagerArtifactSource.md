---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: dcd8d4164d091564aef3d3802430ab499eac38ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115351"
---
# <span data-ttu-id="9c2f5-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9c2f5-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="9c2f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9c2f5-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2f5-103">Cria uma fonte de artefatos.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-103">Creates an artifact source.</span></span>

## <span data-ttu-id="9c2f5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9c2f5-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c2f5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c2f5-105">DESCRIPTION</span></span>
<span data-ttu-id="9c2f5-106">O **cmdlet New-AzDeploymentManagerArtifactSource** cria uma fonte de artefatos.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="9c2f5-107">*Especifique o Nome,* *ResourceGroupName* e as propriedades necessárias.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="9c2f5-108">Você pode modificar o objeto retornado localmente e, em seguida, aplicar as alterações à origem do artefato usando o cmdlet Set-AzDeploymentManagerArtifactSource texto.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="9c2f5-109">O cmdlet retorna um objeto ArtifactSource que tem uma ResourceId que pode ser referenciada no cmdlet New-AzDeploymentManagerServiceTopology para que artefatos necessários para um recurso ServiceUnit, os arquivos Modelo e Parâmetros, possam ser referenciados a partir desse local.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="9c2f5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9c2f5-110">EXAMPLES</span></span>

### <span data-ttu-id="9c2f5-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9c2f5-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="9c2f5-112">Cria uma fonte de artefatos no Grupo ContosoResource com o nome ContosoArtifactSource com Central US como o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="9c2f5-113">A propriedade SasUri fornece um Uri SAS de armazenamento do Azure para o contêiner de armazenamento onde os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="9c2f5-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c2f5-114">PARAMETERS</span></span>

### <span data-ttu-id="9c2f5-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="9c2f5-115">-ArtifactRoot</span></span>
<span data-ttu-id="9c2f5-116">O deslocamento opcional do diretório sob o contêiner de armazenamento dos artefatos.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="9c2f5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2f5-117">-DefaultProfile</span></span>
<span data-ttu-id="9c2f5-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c2f5-119">-Local</span><span class="sxs-lookup"><span data-stu-id="9c2f5-119">-Location</span></span>
<span data-ttu-id="9c2f5-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2f5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9c2f5-121">-Name</span></span>
<span data-ttu-id="9c2f5-122">O nome da origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2f5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c2f5-123">-ResourceGroupName</span></span>
<span data-ttu-id="9c2f5-124">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2f5-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="9c2f5-125">-SasUri</span></span>
<span data-ttu-id="9c2f5-126">O SAS Uri para o contêiner de armazenamento do Azure onde os artefatos são armazenados.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c2f5-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c2f5-127">-Tag</span></span>
<span data-ttu-id="9c2f5-128">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c2f5-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="9c2f5-129">-Confirm</span></span>
<span data-ttu-id="9c2f5-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c2f5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2f5-131">-WhatIf</span></span>
<span data-ttu-id="9c2f5-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c2f5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c2f5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2f5-134">CommonParameters</span></span>
<span data-ttu-id="9c2f5-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c2f5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2f5-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9c2f5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2f5-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="9c2f5-137">INPUTS</span></span>

### <span data-ttu-id="9c2f5-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c2f5-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9c2f5-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="9c2f5-139">OUTPUTS</span></span>

### <span data-ttu-id="9c2f5-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="9c2f5-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="9c2f5-141">Notas</span><span class="sxs-lookup"><span data-stu-id="9c2f5-141">NOTES</span></span>

## <span data-ttu-id="9c2f5-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9c2f5-142">RELATED LINKS</span></span>
