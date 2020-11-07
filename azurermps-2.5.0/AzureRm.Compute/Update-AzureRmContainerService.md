---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 43D01A97-75B9-46CE-B007-26FE6A97C31C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 9a199a0aa0e31cf8bc57585d4825a33e10b5bfc1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786540"
---
# <span data-ttu-id="b49ac-101">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b49ac-101">Update-AzureRmContainerService</span></span>

## <span data-ttu-id="b49ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b49ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b49ac-103">Atualiza o estado de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="b49ac-103">Updates the state of a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b49ac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b49ac-104">SYNTAX</span></span>

```
Update-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b49ac-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b49ac-105">DESCRIPTION</span></span>
<span data-ttu-id="b49ac-106">O cmdlet **Update-AzureRmContainerService** atualiza o estado de um serviço de contêiner para corresponder a uma instância local do serviço.</span><span class="sxs-lookup"><span data-stu-id="b49ac-106">The **Update-AzureRmContainerService** cmdlet updates the state of a container service to match a local instance of the service.</span></span>

## <span data-ttu-id="b49ac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b49ac-107">EXAMPLES</span></span>

### <span data-ttu-id="b49ac-108">Exemplo 1: atualizar um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="b49ac-108">Example 1: Update a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" | Remove-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17" -Count 2 | Update-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="b49ac-109">Esse comando obtém o serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzureRmContainerService.</span><span class="sxs-lookup"><span data-stu-id="b49ac-109">This command gets the container service named CSResourceGroup17 by using the Get-AzureRmContainerService cmdlet.</span></span>
<span data-ttu-id="b49ac-110">O comando passa esse objeto para o cmdlet Remove-AzureRmContainerServiceAgentPoolProfile usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="b49ac-110">The command passes that object to the Remove-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="b49ac-111">**Remove-AzureRmContainerServiceAgentPoolProfile** remove o perfil chamado AgentPool01.</span><span class="sxs-lookup"><span data-stu-id="b49ac-111">**Remove-AzureRmContainerServiceAgentPoolProfile** removes the profile named AgentPool01.</span></span>
<span data-ttu-id="b49ac-112">O comando passa o resultado para o cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="b49ac-112">The command passes the result to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

<span data-ttu-id="b49ac-113">**Add-AzureRmContainerServiceAgentPoolProfile** adiciona um perfil que tem o nome AgentPool01 e tem as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="b49ac-113">**Add-AzureRmContainerServiceAgentPoolProfile** adds a profile that has the name AgentPool01, and has the specified properties.</span></span>
<span data-ttu-id="b49ac-114">O comando passa o resultado para o cmdlet atual.</span><span class="sxs-lookup"><span data-stu-id="b49ac-114">The command passes the result to the current cmdlet.</span></span>

<span data-ttu-id="b49ac-115">O cmdlet atual atualiza o serviço de contêiner para refletir as alterações feitas neste comando.</span><span class="sxs-lookup"><span data-stu-id="b49ac-115">The current cmdlet updates the container service to reflect the changes that were made in this command.</span></span>

## <span data-ttu-id="b49ac-116">OS</span><span class="sxs-lookup"><span data-stu-id="b49ac-116">PARAMETERS</span></span>

### <span data-ttu-id="b49ac-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b49ac-117">-AsJob</span></span>
<span data-ttu-id="b49ac-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="b49ac-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b49ac-119">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="b49ac-119">-ContainerService</span></span>
<span data-ttu-id="b49ac-120">Especifica um objeto **ContainerService** local que contém alterações.</span><span class="sxs-lookup"><span data-stu-id="b49ac-120">Specifies a local **ContainerService** object that contains changes.</span></span>

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b49ac-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b49ac-121">-DefaultProfile</span></span>
<span data-ttu-id="b49ac-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b49ac-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b49ac-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b49ac-123">-Name</span></span>
<span data-ttu-id="b49ac-124">Especifica o nome do serviço de contêiner que este cmdlet atualiza.</span><span class="sxs-lookup"><span data-stu-id="b49ac-124">Specifies the name of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b49ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="b49ac-126">Especifica o grupo de recursos do serviço de contêiner em que este cmdlet é atualizado.</span><span class="sxs-lookup"><span data-stu-id="b49ac-126">Specifies the resource group of the container service that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b49ac-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b49ac-127">-Confirm</span></span>
<span data-ttu-id="b49ac-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b49ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b49ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b49ac-129">-WhatIf</span></span>
<span data-ttu-id="b49ac-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b49ac-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b49ac-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b49ac-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b49ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b49ac-132">CommonParameters</span></span>
<span data-ttu-id="b49ac-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b49ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b49ac-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b49ac-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b49ac-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b49ac-135">INPUTS</span></span>

### <span data-ttu-id="b49ac-136">ContainerService</span><span class="sxs-lookup"><span data-stu-id="b49ac-136">ContainerService</span></span>
<span data-ttu-id="b49ac-137">O parâmetro ' ContainerService ' aceita o valor do tipo ' ContainerService ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="b49ac-137">Parameter 'ContainerService' accepts value of type 'ContainerService' from the pipeline</span></span>

## <span data-ttu-id="b49ac-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b49ac-138">OUTPUTS</span></span>

### <span data-ttu-id="b49ac-139">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="b49ac-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="b49ac-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b49ac-140">NOTES</span></span>

## <span data-ttu-id="b49ac-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b49ac-141">RELATED LINKS</span></span>

[<span data-ttu-id="b49ac-142">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b49ac-142">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="b49ac-143">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b49ac-143">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="b49ac-144">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b49ac-144">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="b49ac-145">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="b49ac-145">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="b49ac-146">Remove-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="b49ac-146">Remove-AzureRmContainerServiceAgentPoolProfile</span></span>](./Remove-AzureRmContainerServiceAgentPoolProfile.md)


