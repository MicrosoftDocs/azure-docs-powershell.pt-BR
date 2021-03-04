---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 9d5d79f65adbcab7ce61ad125e78189d0f84f9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888960"
---
# <span data-ttu-id="b90b1-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b90b1-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b90b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b90b1-102">SYNOPSIS</span></span>
<span data-ttu-id="b90b1-103">Atualiza a origem dos artefatos.</span><span class="sxs-lookup"><span data-stu-id="b90b1-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="b90b1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b90b1-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b90b1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b90b1-105">DESCRIPTION</span></span>
<span data-ttu-id="b90b1-106">O cmdlet **Set-AzDeploymentManagerArtifactSource** atualiza uma fonte de artefato com o objeto de origem de artefato especificado.</span><span class="sxs-lookup"><span data-stu-id="b90b1-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="b90b1-107">O cmdlet retorna o objeto ArtifactSource atualizado.</span><span class="sxs-lookup"><span data-stu-id="b90b1-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="b90b1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b90b1-108">EXAMPLES</span></span>

### <span data-ttu-id="b90b1-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b90b1-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="b90b1-110">Este comando atualiza uma fonte de artefato cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b90b1-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="b90b1-111">A origem do artefato seria atualizada para as propriedades definidas no $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="b90b1-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="b90b1-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b90b1-112">PARAMETERS</span></span>

### <span data-ttu-id="b90b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90b1-113">-DefaultProfile</span></span>
<span data-ttu-id="b90b1-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b90b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b90b1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b90b1-115">-InputObject</span></span>
<span data-ttu-id="b90b1-116">O objeto de origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="b90b1-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b90b1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b90b1-117">-Confirm</span></span>
<span data-ttu-id="b90b1-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b90b1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b90b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b90b1-119">-WhatIf</span></span>
<span data-ttu-id="b90b1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b90b1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b90b1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b90b1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b90b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90b1-122">CommonParameters</span></span>
<span data-ttu-id="b90b1-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b90b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90b1-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b90b1-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90b1-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b90b1-125">INPUTS</span></span>

### <span data-ttu-id="b90b1-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b90b1-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b90b1-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b90b1-127">OUTPUTS</span></span>

### <span data-ttu-id="b90b1-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b90b1-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b90b1-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="b90b1-129">NOTES</span></span>

## <span data-ttu-id="b90b1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b90b1-130">RELATED LINKS</span></span>
