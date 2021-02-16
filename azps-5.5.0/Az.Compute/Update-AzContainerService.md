---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzContainerService.md
ms.openlocfilehash: 199b61bc8ef075aabc09870cde436a0e49598ee8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127070"
---
# <span data-ttu-id="003cd-101">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="003cd-101">Update-AzContainerService</span></span>

## <span data-ttu-id="003cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="003cd-102">SYNOPSIS</span></span>
<span data-ttu-id="003cd-103">Atualiza o estado de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="003cd-103">Updates the state of a container service.</span></span>

## <span data-ttu-id="003cd-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="003cd-104">SYNTAX</span></span>

```
Update-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="003cd-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="003cd-105">DESCRIPTION</span></span>
<span data-ttu-id="003cd-106">O cmdlet **Update-AzContainerService** atualiza o estado de um serviço de contêiner para corresponder a uma instância local do serviço.</span><span class="sxs-lookup"><span data-stu-id="003cd-106">The **Update-AzContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="003cd-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="003cd-107">EXAMPLES</span></span>

### <span data-ttu-id="003cd-108">Exemplo 1: Atualizar um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="003cd-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="003cd-109">Esse comando obtém o serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzContainerService contêiner.</span><span class="sxs-lookup"><span data-stu-id="003cd-109">This command gets the container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="003cd-110">O comando passa esse objeto para o Remove-AzContainerServiceAgentPoolProfile cmdlet usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="003cd-110">The command passes that object to the Remove-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="003cd-111">**Remove-AzContainerServiceAgentPoolProfile** remove o perfil chamado AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="003cd-111">**Remove-AzContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="003cd-112">O comando passa o resultado para o Add-AzContainerServiceAgentPoolProfile cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003cd-112">The command passes the result to the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>
<span data-ttu-id="003cd-113">**O Add-AzContainerServiceAgentPoolProfile** adiciona um perfil que tem o nome AgentPool01 e tem as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="003cd-113">**Add-AzContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="003cd-114">O comando passa o resultado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="003cd-114">The command passes the result to the current cmdlet.</span></span>
<span data-ttu-id="003cd-115">O cmdlet atual atualiza o serviço de contêiner para refletir as alterações feitas neste comando.</span><span class="sxs-lookup"><span data-stu-id="003cd-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="003cd-116">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="003cd-116">PARAMETERS</span></span>

### <span data-ttu-id="003cd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="003cd-117">-AsJob</span></span>
<span data-ttu-id="003cd-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="003cd-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="003cd-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="003cd-119">-ContainerService</span></span>
<span data-ttu-id="003cd-120">Especifica um objeto **ContainerService** local que contém alterações.</span><span class="sxs-lookup"><span data-stu-id="003cd-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="003cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003cd-121">-DefaultProfile</span></span>
<span data-ttu-id="003cd-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="003cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="003cd-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="003cd-123">-Name</span></span>
<span data-ttu-id="003cd-124">Especifica o nome do serviço de contêiner que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="003cd-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="003cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="003cd-126">Especifica o grupo de recursos do serviço de contêineres que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="003cd-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="003cd-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="003cd-127">-Confirm</span></span>
<span data-ttu-id="003cd-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="003cd-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003cd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="003cd-129">-WhatIf</span></span>
<span data-ttu-id="003cd-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="003cd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="003cd-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="003cd-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="003cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003cd-132">CommonParameters</span></span>
<span data-ttu-id="003cd-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="003cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003cd-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="003cd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003cd-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="003cd-135">INPUTS</span></span>

### <span data-ttu-id="003cd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="003cd-136">System.String</span></span>

### <span data-ttu-id="003cd-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="003cd-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="003cd-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="003cd-138">OUTPUTS</span></span>

### <span data-ttu-id="003cd-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="003cd-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="003cd-140">Notas</span><span class="sxs-lookup"><span data-stu-id="003cd-140">NOTES</span></span>

## <span data-ttu-id="003cd-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="003cd-141">RELATED LINKS</span></span>

[<span data-ttu-id="003cd-142">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="003cd-142">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="003cd-143">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="003cd-143">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="003cd-144">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="003cd-144">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="003cd-145">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="003cd-145">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="003cd-146">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="003cd-146">Remove-AzContainerServiceAgentPoolProfile</span></span>](./Remove-AzContainerServiceAgentPoolProfile.md)


