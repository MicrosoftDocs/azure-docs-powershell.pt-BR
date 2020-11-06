---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmContainerService.md
ms.openlocfilehash: ca6a89f7818760a6bab65e45fec703c00d8e7f8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441149"
---
# <span data-ttu-id="3eb4d-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb4d-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="3eb4d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3eb4d-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb4d-103">Atualiza o estado de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb4d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3eb4d-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3eb4d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3eb4d-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb4d-106">O cmdlet **Update-AzureRmContainerService** atualiza o estado de um serviço de contêiner para corresponder a uma instância local do serviço.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="3eb4d-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3eb4d-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb4d-108">Exemplo 1: atualizar um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="3eb4d-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="3eb4d-109">Esse comando obtém o serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="3eb4d-110">O comando passa esse objeto para o cmdlet Remove-AzureRmContainerServiceAgentPoolProfile usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="3eb4d-111">**Remove-AzureRmContainerServiceAgentPoolProfile** remove o perfil chamado AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="3eb4d-112">O comando passa o resultado para o cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="3eb4d-113">**Add-AzureRmContainerServiceAgentPoolProfile** adiciona um perfil que tem o nome AgentPool01 e tem as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="3eb4d-114">O comando passa o resultado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="3eb4d-115">O cmdlet atual atualiza o serviço de contêiner para refletir as alterações feitas neste comando.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="3eb4d-116">OS</span><span class="sxs-lookup"><span data-stu-id="3eb4d-116">PARAMETERS</span></span>

### <span data-ttu-id="3eb4d-117">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb4d-117">-ContainerService</span></span>
<span data-ttu-id="3eb4d-118">Especifica um objeto **ContainerService** local que contém alterações.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-118">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb4d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb4d-119">-DefaultProfile</span></span>
<span data-ttu-id="3eb4d-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eb4d-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3eb4d-121">-Name</span></span>
<span data-ttu-id="3eb4d-122">Especifica o nome do serviço de contêiner que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-122">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eb4d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb4d-123">-ResourceGroupName</span></span>
<span data-ttu-id="3eb4d-124">Especifica o grupo de recursos do serviço de contêiner em que este cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-124">Specifies the resource group of the container service that this cmdlet updates.</span></span>

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

### <span data-ttu-id="3eb4d-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3eb4d-125">-Confirm</span></span>
<span data-ttu-id="3eb4d-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb4d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb4d-127">-WhatIf</span></span>
<span data-ttu-id="3eb4d-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="3eb4d-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb4d-130">CommonParameters</span></span>
<span data-ttu-id="3eb4d-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb4d-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb4d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb4d-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3eb4d-133">INPUTS</span></span>

## <span data-ttu-id="3eb4d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3eb4d-134">OUTPUTS</span></span>

## <span data-ttu-id="3eb4d-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3eb4d-135">NOTES</span></span>

## <span data-ttu-id="3eb4d-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3eb4d-136">RELATED LINKS</span></span>

[<span data-ttu-id="3eb4d-137">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="3eb4d-137">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="3eb4d-138">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb4d-138">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="3eb4d-139">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb4d-139">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="3eb4d-140">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="3eb4d-140">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="3eb4d-141">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="3eb4d-141">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


