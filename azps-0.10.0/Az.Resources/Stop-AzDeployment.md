---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-Azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: 34815482b9729bcac30183cdc18d19c84a2f6628
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776306"
---
# <span data-ttu-id="29c79-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="29c79-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="29c79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="29c79-102">SYNOPSIS</span></span>
<span data-ttu-id="29c79-103">Cancal uma implantação em execução</span><span class="sxs-lookup"><span data-stu-id="29c79-103">Cancal a running deployment</span></span>

## <span data-ttu-id="29c79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29c79-104">SYNTAX</span></span>

### <span data-ttu-id="29c79-105">StopByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="29c79-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c79-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="29c79-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29c79-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="29c79-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29c79-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="29c79-108">DESCRIPTION</span></span>
<span data-ttu-id="29c79-109">O cmdlet **Stop-AzDeployment** cancela uma implantação em escopo de assinatura que foi iniciado, mas não foi concluído.</span><span class="sxs-lookup"><span data-stu-id="29c79-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="29c79-110">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="29c79-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="29c79-111">Para criar uma implantação em escopo de assinatura, use o cmdlet New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="29c79-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="29c79-112">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="29c79-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="29c79-113">Use o parâmetro *Name* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="29c79-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="29c79-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="29c79-114">EXAMPLES</span></span>

### <span data-ttu-id="29c79-115">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29c79-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="29c79-116">Esse comando cancela uma implantação em execução "deployment01" no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="29c79-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="29c79-117">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29c79-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="29c79-118">Esse comando obtém a implantação "deployment01" no escopo da assinatura atual e a cancela.</span><span class="sxs-lookup"><span data-stu-id="29c79-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="29c79-119">OS</span><span class="sxs-lookup"><span data-stu-id="29c79-119">PARAMETERS</span></span>

### <span data-ttu-id="29c79-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="29c79-120">-ApiVersion</span></span>
<span data-ttu-id="29c79-121">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="29c79-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="29c79-122">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="29c79-122">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c79-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c79-123">-DefaultProfile</span></span>
<span data-ttu-id="29c79-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="29c79-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c79-125">-ID</span><span class="sxs-lookup"><span data-stu-id="29c79-125">-Id</span></span>
<span data-ttu-id="29c79-126">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="29c79-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="29c79-127">exemplo:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="29c79-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c79-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29c79-128">-InputObject</span></span>
<span data-ttu-id="29c79-129">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="29c79-129">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29c79-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="29c79-130">-Name</span></span>
<span data-ttu-id="29c79-131">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="29c79-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c79-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29c79-132">-PassThru</span></span>
<span data-ttu-id="29c79-133">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="29c79-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="29c79-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="29c79-134">-Pre</span></span>
<span data-ttu-id="29c79-135">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="29c79-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="29c79-136">-Confirme</span><span class="sxs-lookup"><span data-stu-id="29c79-136">-Confirm</span></span>
<span data-ttu-id="29c79-137">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29c79-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c79-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29c79-138">-WhatIf</span></span>
<span data-ttu-id="29c79-139">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="29c79-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29c79-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="29c79-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29c79-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c79-141">CommonParameters</span></span>
<span data-ttu-id="29c79-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29c79-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29c79-143">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c79-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c79-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="29c79-144">INPUTS</span></span>

### <span data-ttu-id="29c79-145">System. String</span><span class="sxs-lookup"><span data-stu-id="29c79-145">System.String</span></span>

## <span data-ttu-id="29c79-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="29c79-146">OUTPUTS</span></span>

### <span data-ttu-id="29c79-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="29c79-147">System.Boolean</span></span>

## <span data-ttu-id="29c79-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="29c79-148">NOTES</span></span>

## <span data-ttu-id="29c79-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="29c79-149">RELATED LINKS</span></span>