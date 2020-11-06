---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 32e5293f7c5bb62711a6510c590aa1ba7f4229b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596639"
---
# <span data-ttu-id="7bcd5-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7bcd5-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="7bcd5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7bcd5-102">SYNOPSIS</span></span>
<span data-ttu-id="7bcd5-103">Atualiza a origem dos artefatos.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="7bcd5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7bcd5-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bcd5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7bcd5-105">DESCRIPTION</span></span>
<span data-ttu-id="7bcd5-106">O cmdlet **set-AzDeploymentManagerArtifactSource** atualiza uma fonte de artefato com o objeto de origem do artefato especificado.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="7bcd5-107">O cmdlet retorna o objeto Artefatory atualizado.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="7bcd5-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7bcd5-108">EXAMPLES</span></span>

### <span data-ttu-id="7bcd5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7bcd5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="7bcd5-110">Esse comando atualiza uma fonte de artefato cujo nome e o nome do participante correspondem às propriedades Name e ResourceGroupName do $artifactSourceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="7bcd5-111">A origem do artefato seria atualizada para as propriedades definidas no $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="7bcd5-112">OS</span><span class="sxs-lookup"><span data-stu-id="7bcd5-112">PARAMETERS</span></span>

### <span data-ttu-id="7bcd5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bcd5-113">-DefaultProfile</span></span>
<span data-ttu-id="7bcd5-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bcd5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bcd5-115">-InputObject</span></span>
<span data-ttu-id="7bcd5-116">O objeto de origem do artefato.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-116">The artifact source object.</span></span>

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

### <span data-ttu-id="7bcd5-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7bcd5-117">-Confirm</span></span>
<span data-ttu-id="7bcd5-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bcd5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bcd5-119">-WhatIf</span></span>
<span data-ttu-id="7bcd5-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bcd5-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bcd5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bcd5-122">CommonParameters</span></span>
<span data-ttu-id="7bcd5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bcd5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bcd5-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bcd5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bcd5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7bcd5-125">INPUTS</span></span>

### <span data-ttu-id="7bcd5-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7bcd5-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7bcd5-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7bcd5-127">OUTPUTS</span></span>

### <span data-ttu-id="7bcd5-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7bcd5-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7bcd5-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7bcd5-129">NOTES</span></span>

## <span data-ttu-id="7bcd5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7bcd5-130">RELATED LINKS</span></span>
