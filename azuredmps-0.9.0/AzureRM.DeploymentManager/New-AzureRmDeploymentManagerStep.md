---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7b04fc95af1ee340e87fa5ed46cbba9f1956d9e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425684"
---
# <span data-ttu-id="1f194-101">New-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="1f194-101">New-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="1f194-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f194-102">SYNOPSIS</span></span>
<span data-ttu-id="1f194-103">Cria uma nova etapa de implantação.</span><span class="sxs-lookup"><span data-stu-id="1f194-103">Creates a new deployment step.</span></span>

## <span data-ttu-id="1f194-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f194-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -Duration <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f194-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f194-105">DESCRIPTION</span></span>
<span data-ttu-id="1f194-106">O cmdlet **New-AzureRmDeploymentManagerStep** cria uma etapa de implantação que pode ser referenciada em implementações.</span><span class="sxs-lookup"><span data-stu-id="1f194-106">The **New-AzureRmDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="1f194-107">Especifique o *nome* , *ResourceGroupName* e propriedades necessárias.</span><span class="sxs-lookup"><span data-stu-id="1f194-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="1f194-108">Você pode modificar o objeto retornado localmente e, em seguida, aplicar as alterações à etapa usando o cmdlet Set-AzureRmDeploymentManagerStep.</span><span class="sxs-lookup"><span data-stu-id="1f194-108">You can modify the returned object locally and then apply the changes to the step by using the Set-AzureRmDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="1f194-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f194-109">EXAMPLES</span></span>

### <span data-ttu-id="1f194-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f194-110">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="1f194-111">Cria uma etapa no ContosoResourceGroup com o nome ContosoService1WaitStep no centro dos EUA como o local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1f194-111">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="1f194-112">A Propriedade Duration fornece a duração que a distribuição aguardará antes de executar a próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="1f194-112">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="1f194-113">OS</span><span class="sxs-lookup"><span data-stu-id="1f194-113">PARAMETERS</span></span>

### <span data-ttu-id="1f194-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f194-114">-DefaultProfile</span></span>
<span data-ttu-id="1f194-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f194-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f194-116">-Duração</span><span class="sxs-lookup"><span data-stu-id="1f194-116">-Duration</span></span>
<span data-ttu-id="1f194-117">A duração a ser esperada no formato ISO 8601.</span><span class="sxs-lookup"><span data-stu-id="1f194-117">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="1f194-118">Por exemplo: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="1f194-118">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="1f194-119">-Local</span><span class="sxs-lookup"><span data-stu-id="1f194-119">-Location</span></span>
<span data-ttu-id="1f194-120">O local do recurso.</span><span class="sxs-lookup"><span data-stu-id="1f194-120">The location of the resource.</span></span>

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

### <span data-ttu-id="1f194-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f194-121">-Name</span></span>
<span data-ttu-id="1f194-122">O nome da etapa.</span><span class="sxs-lookup"><span data-stu-id="1f194-122">The name of the step.</span></span>

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

### <span data-ttu-id="1f194-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f194-123">-ResourceGroupName</span></span>
<span data-ttu-id="1f194-124">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f194-124">The resource group.</span></span>

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

### <span data-ttu-id="1f194-125">-Marca</span><span class="sxs-lookup"><span data-stu-id="1f194-125">-Tag</span></span>
<span data-ttu-id="1f194-126">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f194-126">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1f194-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f194-127">-Confirm</span></span>
<span data-ttu-id="1f194-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f194-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f194-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f194-129">-WhatIf</span></span>
<span data-ttu-id="1f194-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f194-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f194-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f194-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f194-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f194-132">CommonParameters</span></span>
<span data-ttu-id="1f194-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f194-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="1f194-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f194-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f194-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f194-135">INPUTS</span></span>

### <span data-ttu-id="1f194-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1f194-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1f194-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f194-137">OUTPUTS</span></span>

### <span data-ttu-id="1f194-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="1f194-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="1f194-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f194-139">NOTES</span></span>

## <span data-ttu-id="1f194-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f194-140">RELATED LINKS</span></span>
