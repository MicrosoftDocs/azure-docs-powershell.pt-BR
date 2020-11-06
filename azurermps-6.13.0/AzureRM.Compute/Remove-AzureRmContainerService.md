---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: 19c94fae0192766b87f430e6137fe8d3652325c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428540"
---
# <span data-ttu-id="c49ae-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c49ae-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="c49ae-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c49ae-102">SYNOPSIS</span></span>
<span data-ttu-id="c49ae-103">Remove um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c49ae-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c49ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c49ae-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c49ae-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c49ae-105">DESCRIPTION</span></span>
<span data-ttu-id="c49ae-106">O cmdlet **Remove-AzureRmContainerService** remove um serviço de contêiner da sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="c49ae-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="c49ae-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c49ae-107">EXAMPLES</span></span>

### <span data-ttu-id="c49ae-108">Exemplo 1: remover um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="c49ae-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="c49ae-109">Esse comando Remove o serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="c49ae-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="c49ae-110">OS</span><span class="sxs-lookup"><span data-stu-id="c49ae-110">PARAMETERS</span></span>

### <span data-ttu-id="c49ae-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c49ae-111">-AsJob</span></span>
<span data-ttu-id="c49ae-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c49ae-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c49ae-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c49ae-113">-DefaultProfile</span></span>
<span data-ttu-id="c49ae-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c49ae-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c49ae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c49ae-115">-Force</span></span>
<span data-ttu-id="c49ae-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c49ae-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c49ae-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c49ae-117">-Name</span></span>
<span data-ttu-id="c49ae-118">Especifica o nome do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c49ae-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c49ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c49ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="c49ae-120">Especifica o grupo de recursos do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c49ae-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c49ae-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c49ae-121">-Confirm</span></span>
<span data-ttu-id="c49ae-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c49ae-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c49ae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c49ae-123">-WhatIf</span></span>
<span data-ttu-id="c49ae-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c49ae-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c49ae-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c49ae-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c49ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c49ae-126">CommonParameters</span></span>
<span data-ttu-id="c49ae-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c49ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c49ae-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c49ae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c49ae-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c49ae-129">INPUTS</span></span>

### <span data-ttu-id="c49ae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c49ae-130">System.String</span></span>

## <span data-ttu-id="c49ae-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c49ae-131">OUTPUTS</span></span>

### <span data-ttu-id="c49ae-132">System. void</span><span class="sxs-lookup"><span data-stu-id="c49ae-132">System.Void</span></span>

## <span data-ttu-id="c49ae-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c49ae-133">NOTES</span></span>

## <span data-ttu-id="c49ae-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c49ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="c49ae-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c49ae-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="c49ae-136">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c49ae-136">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="c49ae-137">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c49ae-137">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


