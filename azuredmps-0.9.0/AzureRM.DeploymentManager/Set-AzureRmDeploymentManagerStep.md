---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerstep
schema: 2.0.0
ms.openlocfilehash: 7241e072109583b7afc24fc3f69746599bd67c53
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425896"
---
# <span data-ttu-id="ae584-101">Set-AzureRmDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="ae584-101">Set-AzureRmDeploymentManagerStep</span></span>

## <span data-ttu-id="ae584-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae584-102">SYNOPSIS</span></span>
<span data-ttu-id="ae584-103">Atualiza uma etapa.</span><span class="sxs-lookup"><span data-stu-id="ae584-103">Updates a step.</span></span>

## <span data-ttu-id="ae584-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae584-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerStep [-Step] <PSStepResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae584-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae584-105">DESCRIPTION</span></span>
<span data-ttu-id="ae584-106">O cmdlet **set-AzureRmDeploymentManagerStep** atualiza uma etapa com o objeto Step especificado.</span><span class="sxs-lookup"><span data-stu-id="ae584-106">The **Set-AzureRmDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="ae584-107">O cmdlet retorna o objeto Step atualizado.</span><span class="sxs-lookup"><span data-stu-id="ae584-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="ae584-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae584-108">EXAMPLES</span></span>

### <span data-ttu-id="ae584-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae584-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerStep -Step $stepObject
```

<span data-ttu-id="ae584-110">Esse comando atualiza uma etapa cujo nome e o meu nome do elemento de Resource correspondem às propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ae584-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="ae584-111">A etapa seria atualizada para as propriedades definidas no $stepObject.</span><span class="sxs-lookup"><span data-stu-id="ae584-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="ae584-112">OS</span><span class="sxs-lookup"><span data-stu-id="ae584-112">PARAMETERS</span></span>

### <span data-ttu-id="ae584-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae584-113">-DefaultProfile</span></span>
<span data-ttu-id="ae584-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae584-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae584-115">-Etapa</span><span class="sxs-lookup"><span data-stu-id="ae584-115">-Step</span></span>
<span data-ttu-id="ae584-116">O objeto Step.</span><span class="sxs-lookup"><span data-stu-id="ae584-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae584-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae584-117">-Confirm</span></span>
<span data-ttu-id="ae584-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae584-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae584-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae584-119">-WhatIf</span></span>
<span data-ttu-id="ae584-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae584-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae584-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae584-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae584-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae584-122">CommonParameters</span></span>
<span data-ttu-id="ae584-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae584-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae584-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae584-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae584-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae584-125">INPUTS</span></span>

### <span data-ttu-id="ae584-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ae584-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ae584-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae584-127">OUTPUTS</span></span>

### <span data-ttu-id="ae584-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="ae584-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="ae584-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae584-129">NOTES</span></span>

## <span data-ttu-id="ae584-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae584-130">RELATED LINKS</span></span>
