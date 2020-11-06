---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 2f4cab266cf63e1c33c35c051e9cc2b838f5b066
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425662"
---
# <span data-ttu-id="d13b1-101">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d13b1-101">Set-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="d13b1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d13b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d13b1-103">Atualiza um serviço na topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="d13b1-103">Updates a service in service topology.</span></span>

## <span data-ttu-id="d13b1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d13b1-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d13b1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d13b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d13b1-106">O cmdlet **set-AzureRmDeploymentManagerService** atualiza um serviço com o objeto de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="d13b1-106">The **Set-AzureRmDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="d13b1-107">O cmdlet retorna o objeto de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="d13b1-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="d13b1-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d13b1-108">EXAMPLES</span></span>

### <span data-ttu-id="d13b1-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d13b1-109">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="d13b1-110">Esse comando atualiza um serviço cujo nome, nome da topologia de serviço e o nome do contato correspondem às propriedades Name, imtopologyname e ResourceGroupName da $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d13b1-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="d13b1-111">O serviço seria atualizado para as propriedades definidas no $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="d13b1-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="d13b1-112">OS</span><span class="sxs-lookup"><span data-stu-id="d13b1-112">PARAMETERS</span></span>

### <span data-ttu-id="d13b1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13b1-113">-DefaultProfile</span></span>
<span data-ttu-id="d13b1-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d13b1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d13b1-115">-Serviço</span><span class="sxs-lookup"><span data-stu-id="d13b1-115">-Service</span></span>
<span data-ttu-id="d13b1-116">O objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="d13b1-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d13b1-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d13b1-117">-Confirm</span></span>
<span data-ttu-id="d13b1-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d13b1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d13b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d13b1-119">-WhatIf</span></span>
<span data-ttu-id="d13b1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d13b1-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d13b1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d13b1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d13b1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13b1-122">CommonParameters</span></span>
<span data-ttu-id="d13b1-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d13b1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13b1-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d13b1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13b1-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d13b1-125">INPUTS</span></span>

### <span data-ttu-id="d13b1-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d13b1-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d13b1-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d13b1-127">OUTPUTS</span></span>

### <span data-ttu-id="d13b1-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d13b1-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d13b1-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d13b1-129">NOTES</span></span>

## <span data-ttu-id="d13b1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d13b1-130">RELATED LINKS</span></span>

[<span data-ttu-id="d13b1-131">New-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d13b1-131">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="d13b1-132">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d13b1-132">Get-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="d13b1-133">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d13b1-133">Remove-AzureRmDeploymentManagerService</span></span>](./Remove-AzureRmDeploymentManagerService.md)