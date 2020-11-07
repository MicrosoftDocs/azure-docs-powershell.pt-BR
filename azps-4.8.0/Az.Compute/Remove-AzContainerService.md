---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93955756"
---
# <span data-ttu-id="95730-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="95730-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="95730-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="95730-102">SYNOPSIS</span></span>
<span data-ttu-id="95730-103">Remove um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="95730-103">Removes a container service.</span></span>

## <span data-ttu-id="95730-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="95730-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95730-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="95730-105">DESCRIPTION</span></span>
<span data-ttu-id="95730-106">O cmdlet **Remove-AzContainerService** remove um serviço de contêiner da sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="95730-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="95730-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="95730-107">EXAMPLES</span></span>

### <span data-ttu-id="95730-108">Exemplo 1: remover um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="95730-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="95730-109">Esse comando Remove o serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="95730-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="95730-110">OS</span><span class="sxs-lookup"><span data-stu-id="95730-110">PARAMETERS</span></span>

### <span data-ttu-id="95730-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95730-111">-AsJob</span></span>
<span data-ttu-id="95730-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="95730-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="95730-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95730-113">-DefaultProfile</span></span>
<span data-ttu-id="95730-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="95730-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95730-115">-Force</span><span class="sxs-lookup"><span data-stu-id="95730-115">-Force</span></span>
<span data-ttu-id="95730-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="95730-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="95730-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="95730-117">-Name</span></span>
<span data-ttu-id="95730-118">Especifica o nome do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="95730-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95730-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95730-119">-ResourceGroupName</span></span>
<span data-ttu-id="95730-120">Especifica o grupo de recursos do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="95730-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="95730-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="95730-121">-Confirm</span></span>
<span data-ttu-id="95730-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95730-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95730-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95730-123">-WhatIf</span></span>
<span data-ttu-id="95730-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="95730-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95730-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="95730-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95730-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95730-126">CommonParameters</span></span>
<span data-ttu-id="95730-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95730-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95730-128">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95730-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95730-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="95730-129">INPUTS</span></span>

### <span data-ttu-id="95730-130">System. String</span><span class="sxs-lookup"><span data-stu-id="95730-130">System.String</span></span>

## <span data-ttu-id="95730-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="95730-131">OUTPUTS</span></span>

### <span data-ttu-id="95730-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="95730-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="95730-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="95730-133">NOTES</span></span>

## <span data-ttu-id="95730-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="95730-134">RELATED LINKS</span></span>

[<span data-ttu-id="95730-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="95730-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="95730-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="95730-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="95730-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="95730-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


