---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: f07b2f59f1a38aca780e1e869bb3904725df6dcd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610719"
---
# <span data-ttu-id="24e76-101">Stop-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="24e76-101">Stop-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="24e76-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="24e76-102">SYNOPSIS</span></span>
<span data-ttu-id="24e76-103">Cancela uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24e76-103">Cancels a resource group deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24e76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="24e76-104">SYNTAX</span></span>

### <span data-ttu-id="24e76-105">O parâmetro de nome de implantação definido.</span><span class="sxs-lookup"><span data-stu-id="24e76-105">The deployment name parameter set.</span></span> <span data-ttu-id="24e76-106">Assume</span><span class="sxs-lookup"><span data-stu-id="24e76-106">(Default)</span></span>
```
Stop-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24e76-107">O conjunto de parâmetros de ID de implantação.</span><span class="sxs-lookup"><span data-stu-id="24e76-107">The deployment Id parameter set.</span></span>
```
Stop-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24e76-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="24e76-108">DESCRIPTION</span></span>
<span data-ttu-id="24e76-109">O cmdlet **Stop-AzureRmResourceGroupDeployment** cancela uma implantação de grupo de recursos do Azure que foi iniciada, mas não foi completada.</span><span class="sxs-lookup"><span data-stu-id="24e76-109">The **Stop-AzureRmResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="24e76-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="24e76-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="24e76-111">Um recurso do Azure é uma entidade gerenciada pelo usuário, como um site da Web, um banco de dados ou um servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="24e76-111">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="24e76-112">Um grupo de recursos é uma coleção de recursos implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="24e76-112">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="24e76-113">Para implantar um grupo de recursos, use o cmdlet New-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="24e76-113">To deploy a resource group, use the New-AzureRmResourceGroupDeployment cmdlet.</span></span>

<span data-ttu-id="24e76-114">O cmdlet New-AzureRmResource cria um novo recurso, mas ele não aciona uma operação de implantação de grupo de recursos que esse cmdlet pode parar.</span><span class="sxs-lookup"><span data-stu-id="24e76-114">The New-AzureRmResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="24e76-115">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="24e76-115">This cmdlet stops only one running deployment.</span></span>

<span data-ttu-id="24e76-116">Use o parâmetro *Name* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="24e76-116">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="24e76-117">Se você omitir o parâmetro *Name* , **Stop-AzureRmResourceGroupDeployment** procurará uma implantação em execução e a interromperá.</span><span class="sxs-lookup"><span data-stu-id="24e76-117">If you omit the *Name* parameter, **Stop-AzureRmResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="24e76-118">Se o cmdlet encontrar mais de uma implantação em execução, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="24e76-118">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="24e76-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="24e76-119">EXAMPLES</span></span>

## <span data-ttu-id="24e76-120">OS</span><span class="sxs-lookup"><span data-stu-id="24e76-120">PARAMETERS</span></span>

### <span data-ttu-id="24e76-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="24e76-121">-ApiVersion</span></span>
<span data-ttu-id="24e76-122">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="24e76-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="24e76-123">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="24e76-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="24e76-124">-ID</span><span class="sxs-lookup"><span data-stu-id="24e76-124">-Id</span></span>
<span data-ttu-id="24e76-125">Especifica a ID da implantação do grupo de recursos a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="24e76-125">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24e76-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="24e76-126">-Name</span></span>
<span data-ttu-id="24e76-127">Especifica o nome da implantação do grupo de recursos a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="24e76-127">Specifies the name of the resource group deployment to stop.</span></span>

<span data-ttu-id="24e76-128">Se você não especificar esse parâmetro, esse cmdlet procurará uma implantação em execução no grupo de recursos e a interromperá.</span><span class="sxs-lookup"><span data-stu-id="24e76-128">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="24e76-129">Se ele encontrar mais de uma implantação em execução, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="24e76-129">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="24e76-130">Para obter o nome da implantação, use o cmdlet Get-AzureRmResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="24e76-130">To get the deployment name, use the Get-AzureRmResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24e76-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="24e76-131">-Pre</span></span>
<span data-ttu-id="24e76-132">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="24e76-132">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="24e76-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e76-133">-ResourceGroupName</span></span>
<span data-ttu-id="24e76-134">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="24e76-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="24e76-135">Esse cmdlet interrompe a implantação do grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="24e76-135">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24e76-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="24e76-136">-Confirm</span></span>
<span data-ttu-id="24e76-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="24e76-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24e76-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24e76-138">-WhatIf</span></span>
<span data-ttu-id="24e76-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="24e76-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24e76-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="24e76-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24e76-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e76-141">-DefaultProfile</span></span>
<span data-ttu-id="24e76-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="24e76-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24e76-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e76-143">CommonParameters</span></span>
<span data-ttu-id="24e76-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e76-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e76-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e76-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e76-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="24e76-146">INPUTS</span></span>

### <span data-ttu-id="24e76-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="24e76-147">None</span></span>

## <span data-ttu-id="24e76-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="24e76-148">OUTPUTS</span></span>

### <span data-ttu-id="24e76-149">Booliana</span><span class="sxs-lookup"><span data-stu-id="24e76-149">Boolean</span></span>

## <span data-ttu-id="24e76-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="24e76-150">NOTES</span></span>

## <span data-ttu-id="24e76-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="24e76-151">RELATED LINKS</span></span>

[<span data-ttu-id="24e76-152">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="24e76-152">Get-AzureRmResourceGroupDeployment</span></span>](./Get-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="24e76-153">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="24e76-153">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="24e76-154">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="24e76-154">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="24e76-155">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="24e76-155">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="24e76-156">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="24e76-156">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="24e76-157">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="24e76-157">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


