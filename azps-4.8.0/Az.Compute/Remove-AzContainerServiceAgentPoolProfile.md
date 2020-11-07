---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955745"
---
# <span data-ttu-id="f02a8-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f02a8-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="f02a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f02a8-102">SYNOPSIS</span></span>
<span data-ttu-id="f02a8-103">Remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f02a8-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="f02a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f02a8-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f02a8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f02a8-105">DESCRIPTION</span></span>
<span data-ttu-id="f02a8-106">O cmdlet **Remove-AzContainerServiceAgentPoolProfile** remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f02a8-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="f02a8-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f02a8-107">EXAMPLES</span></span>

### <span data-ttu-id="f02a8-108">Exemplo 1: remover um perfil de um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="f02a8-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="f02a8-109">O primeiro comando obtém um serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzContainerService.</span><span class="sxs-lookup"><span data-stu-id="f02a8-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="f02a8-110">O comando armazena o serviço na variável $Container.</span><span class="sxs-lookup"><span data-stu-id="f02a8-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="f02a8-111">O segundo comando Remove o perfil chamado AgentPool01 do serviço de contêiner em $Container.</span><span class="sxs-lookup"><span data-stu-id="f02a8-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="f02a8-112">OS</span><span class="sxs-lookup"><span data-stu-id="f02a8-112">PARAMETERS</span></span>

### <span data-ttu-id="f02a8-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="f02a8-113">-ContainerService</span></span>
<span data-ttu-id="f02a8-114">Especifica o objeto de serviço de contêiner do qual esse cmdlet Remove um perfil de pool do agente.</span><span class="sxs-lookup"><span data-stu-id="f02a8-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f02a8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f02a8-115">-DefaultProfile</span></span>
<span data-ttu-id="f02a8-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f02a8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f02a8-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f02a8-117">-Name</span></span>
<span data-ttu-id="f02a8-118">Especifica o nome do perfil do pool de agentes que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="f02a8-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f02a8-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f02a8-119">-Confirm</span></span>
<span data-ttu-id="f02a8-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f02a8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f02a8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f02a8-121">-WhatIf</span></span>
<span data-ttu-id="f02a8-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f02a8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f02a8-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f02a8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f02a8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f02a8-124">CommonParameters</span></span>
<span data-ttu-id="f02a8-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f02a8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f02a8-126">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f02a8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f02a8-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f02a8-127">INPUTS</span></span>

### <span data-ttu-id="f02a8-128">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f02a8-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="f02a8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f02a8-129">System.String</span></span>

## <span data-ttu-id="f02a8-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f02a8-130">OUTPUTS</span></span>

### <span data-ttu-id="f02a8-131">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="f02a8-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="f02a8-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f02a8-132">NOTES</span></span>

## <span data-ttu-id="f02a8-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f02a8-133">RELATED LINKS</span></span>

[<span data-ttu-id="f02a8-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="f02a8-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="f02a8-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="f02a8-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


