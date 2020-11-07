---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 27d1e45a9e2c85fb3d2f7470db97ce2426f62a19
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786150"
---
# <span data-ttu-id="c8f50-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c8f50-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="c8f50-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8f50-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f50-103">Remove um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="c8f50-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f50-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c8f50-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8f50-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c8f50-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f50-106">O cmdlet **Remove-AzureRmContainerService** remove um serviço de contêiner da sua conta do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f50-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="c8f50-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c8f50-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f50-108">Exemplo 1: remover um serviço de contêiner</span><span class="sxs-lookup"><span data-stu-id="c8f50-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="c8f50-109">Esse comando Remove o serviço de contêiner chamado CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="c8f50-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="c8f50-110">OS</span><span class="sxs-lookup"><span data-stu-id="c8f50-110">PARAMETERS</span></span>

### <span data-ttu-id="c8f50-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8f50-111">-AsJob</span></span>
<span data-ttu-id="c8f50-112">Execute o cmdlet em segundo plano e retorne um trabalho para acompanhar o progresso.</span><span class="sxs-lookup"><span data-stu-id="c8f50-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c8f50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f50-113">-DefaultProfile</span></span>
<span data-ttu-id="c8f50-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8f50-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8f50-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c8f50-115">-Force</span></span>
<span data-ttu-id="c8f50-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c8f50-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c8f50-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8f50-117">-Name</span></span>
<span data-ttu-id="c8f50-118">Especifica o nome do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c8f50-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8f50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8f50-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8f50-120">Especifica o grupo de recursos do serviço de contêiner que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="c8f50-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c8f50-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c8f50-121">-Confirm</span></span>
<span data-ttu-id="c8f50-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8f50-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="c8f50-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8f50-123">-WhatIf</span></span>
<span data-ttu-id="c8f50-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c8f50-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8f50-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8f50-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="c8f50-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f50-126">CommonParameters</span></span>
<span data-ttu-id="c8f50-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f50-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f50-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f50-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f50-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c8f50-129">INPUTS</span></span>

### <span data-ttu-id="c8f50-130">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="c8f50-130">None</span></span>
<span data-ttu-id="c8f50-131">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="c8f50-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8f50-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c8f50-132">OUTPUTS</span></span>

### <span data-ttu-id="c8f50-133">System. void</span><span class="sxs-lookup"><span data-stu-id="c8f50-133">System.Void</span></span>

## <span data-ttu-id="c8f50-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c8f50-134">NOTES</span></span>

## <span data-ttu-id="c8f50-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8f50-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8f50-136">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c8f50-136">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="c8f50-137">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c8f50-137">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="c8f50-138">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="c8f50-138">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


