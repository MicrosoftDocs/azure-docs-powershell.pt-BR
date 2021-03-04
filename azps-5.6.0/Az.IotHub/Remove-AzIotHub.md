---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 78478b28e42302ad3a672a0ee889f03807f3d1ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889670"
---
# <span data-ttu-id="415a1-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="415a1-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="415a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="415a1-102">SYNOPSIS</span></span>
<span data-ttu-id="415a1-103">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="415a1-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="415a1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="415a1-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="415a1-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="415a1-105">DESCRIPTION</span></span>
<span data-ttu-id="415a1-106">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="415a1-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="415a1-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="415a1-107">EXAMPLES</span></span>

### <span data-ttu-id="415a1-108">Exemplo 1 Remover um IotHub</span><span class="sxs-lookup"><span data-stu-id="415a1-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="415a1-109">Remove um IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="415a1-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="415a1-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="415a1-110">PARAMETERS</span></span>

### <span data-ttu-id="415a1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415a1-111">-DefaultProfile</span></span>
<span data-ttu-id="415a1-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="415a1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="415a1-113">-Name</span><span class="sxs-lookup"><span data-stu-id="415a1-113">-Name</span></span>
<span data-ttu-id="415a1-114">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="415a1-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="415a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="415a1-116">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="415a1-116">Resource Group Name</span></span>

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

### <span data-ttu-id="415a1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="415a1-117">-Confirm</span></span>
<span data-ttu-id="415a1-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="415a1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="415a1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="415a1-119">-WhatIf</span></span>
<span data-ttu-id="415a1-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="415a1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="415a1-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="415a1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="415a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415a1-122">CommonParameters</span></span>
<span data-ttu-id="415a1-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="415a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415a1-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="415a1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415a1-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="415a1-125">INPUTS</span></span>

### <span data-ttu-id="415a1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="415a1-126">System.String</span></span>

## <span data-ttu-id="415a1-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="415a1-127">OUTPUTS</span></span>

### <span data-ttu-id="415a1-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="415a1-128">System.Void</span></span>

## <span data-ttu-id="415a1-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="415a1-129">NOTES</span></span>

## <span data-ttu-id="415a1-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="415a1-130">RELATED LINKS</span></span>
