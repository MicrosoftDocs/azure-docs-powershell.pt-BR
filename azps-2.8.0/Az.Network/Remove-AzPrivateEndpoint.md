---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpoint.md
ms.openlocfilehash: 1ad9ff225871cde9104a346bd758f2716f630bc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771509"
---
# <span data-ttu-id="ed532-101">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed532-101">Remove-AzPrivateEndpoint</span></span>

## <span data-ttu-id="ed532-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed532-102">SYNOPSIS</span></span>
<span data-ttu-id="ed532-103">Remove um ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="ed532-103">Removes a private endpoint.</span></span>

## <span data-ttu-id="ed532-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed532-104">SYNTAX</span></span>

```
Remove-AzPrivateEndpoint -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed532-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed532-105">DESCRIPTION</span></span>
<span data-ttu-id="ed532-106">O cmdlet **Remove-AzPrivateEndpoint** remove um ponto de extremidade particular.</span><span class="sxs-lookup"><span data-stu-id="ed532-106">The **Remove-AzPrivateEndpoint** cmdlet removes a private endpoint.</span></span> 

## <span data-ttu-id="ed532-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed532-107">EXAMPLES</span></span>

### <span data-ttu-id="ed532-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ed532-108">Example 1</span></span>
```
Remove-AzPrivateEndpoint -Name MyPrivateEndpoint1 -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="ed532-109">Este exemplo remove um ponto de extremidade particular chamado MyPrivateEndpoint1.</span><span class="sxs-lookup"><span data-stu-id="ed532-109">This example remove a private endpoint named MyPrivateEndpoint1.</span></span>

## <span data-ttu-id="ed532-110">OS</span><span class="sxs-lookup"><span data-stu-id="ed532-110">PARAMETERS</span></span>

### <span data-ttu-id="ed532-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ed532-111">-AsJob</span></span>
<span data-ttu-id="ed532-112">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ed532-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ed532-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed532-113">-DefaultProfile</span></span>
<span data-ttu-id="ed532-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed532-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed532-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ed532-115">-Force</span></span>
<span data-ttu-id="ed532-116">Não pedir confirmação se quiser excluir o recurso</span><span class="sxs-lookup"><span data-stu-id="ed532-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ed532-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed532-117">-Name</span></span>
<span data-ttu-id="ed532-118">O nome do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="ed532-118">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed532-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed532-119">-PassThru</span></span>
<span data-ttu-id="ed532-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="ed532-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ed532-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="ed532-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed532-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed532-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed532-123">O nome do grupo de recursos do ponto de extremidade privado.</span><span class="sxs-lookup"><span data-stu-id="ed532-123">The resource group name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed532-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed532-124">-Confirm</span></span>
<span data-ttu-id="ed532-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed532-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed532-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed532-126">-WhatIf</span></span>
<span data-ttu-id="ed532-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed532-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed532-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed532-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed532-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed532-129">CommonParameters</span></span>
<span data-ttu-id="ed532-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed532-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed532-131">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed532-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed532-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed532-132">INPUTS</span></span>

### <span data-ttu-id="ed532-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ed532-133">System.String</span></span>

## <span data-ttu-id="ed532-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed532-134">OUTPUTS</span></span>

### <span data-ttu-id="ed532-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed532-135">System.Boolean</span></span>

## <span data-ttu-id="ed532-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed532-136">NOTES</span></span>

## <span data-ttu-id="ed532-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed532-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed532-138">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed532-138">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="ed532-139">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="ed532-139">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)