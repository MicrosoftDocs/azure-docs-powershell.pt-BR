---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 2013f1722ee246db023f4d26d456eafffa8f40eb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600991"
---
# <span data-ttu-id="8a52d-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="8a52d-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="8a52d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8a52d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a52d-103">Cria uma etapa.</span><span class="sxs-lookup"><span data-stu-id="8a52d-103">Creates a step.</span></span>

## <span data-ttu-id="8a52d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a52d-104">SYNTAX</span></span>

```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a52d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8a52d-105">DESCRIPTION</span></span>
<span data-ttu-id="8a52d-106">O cmdlet **New-AzDeploymentManagerStep** cria uma etapa de implantação que pode ser referenciada em implementações.</span><span class="sxs-lookup"><span data-stu-id="8a52d-106">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="8a52d-107">Especifique o *nome* , *ResourceGroupName* e propriedades necessárias.</span><span class="sxs-lookup"><span data-stu-id="8a52d-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="8a52d-108">Você pode modificar o objeto retornado localmente e, em seguida, aplicar as alterações à etapa usando o cmdlet Set-AzDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="8a52d-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="8a52d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8a52d-109">EXAMPLES</span></span>

### <span data-ttu-id="8a52d-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8a52d-110">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="8a52d-111">Cria uma etapa no ContosoResourceGroup com o nome ContosoService1WaitStep no centro dos EUA como o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8a52d-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="8a52d-112">A Propriedade Duration fornece a duração que a distribuição aguardará antes de executar a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="8a52d-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="8a52d-113">OS</span><span class="sxs-lookup"><span data-stu-id="8a52d-113">PARAMETERS</span></span>

### <span data-ttu-id="8a52d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a52d-114">-DefaultProfile</span></span>
<span data-ttu-id="8a52d-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8a52d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a52d-116">-Duração</span><span class="sxs-lookup"><span data-stu-id="8a52d-116">-Duration</span></span>
<span data-ttu-id="8a52d-117">A duração a ser esperada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="8a52d-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="8a52d-118">Por exemplo: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="8a52d-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="8a52d-119">-Local</span><span class="sxs-lookup"><span data-stu-id="8a52d-119">-Location</span></span>
<span data-ttu-id="8a52d-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="8a52d-120">The location of the resource.</span></span>

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

### <span data-ttu-id="8a52d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a52d-121">-Name</span></span>
<span data-ttu-id="8a52d-122">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="8a52d-122">The name of the step.</span></span>

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

### <span data-ttu-id="8a52d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a52d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a52d-124">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a52d-124">The resource group.</span></span>

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

### <span data-ttu-id="8a52d-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="8a52d-125">-Tag</span></span>
<span data-ttu-id="8a52d-126">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="8a52d-126">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="8a52d-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8a52d-127">-Confirm</span></span>
<span data-ttu-id="8a52d-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a52d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a52d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a52d-129">-WhatIf</span></span>
<span data-ttu-id="8a52d-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8a52d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a52d-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8a52d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a52d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a52d-132">CommonParameters</span></span>
<span data-ttu-id="8a52d-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a52d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a52d-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a52d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a52d-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8a52d-135">INPUTS</span></span>

### <span data-ttu-id="8a52d-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8a52d-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8a52d-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8a52d-137">OUTPUTS</span></span>

### <span data-ttu-id="8a52d-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="8a52d-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="8a52d-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8a52d-139">NOTES</span></span>

## <span data-ttu-id="8a52d-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8a52d-140">RELATED LINKS</span></span>
