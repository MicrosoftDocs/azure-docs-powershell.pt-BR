---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 4e851c6a65e2ff69e6675a2e057a1ed319ba6519
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98258885"
---
# <span data-ttu-id="4b5c5-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="4b5c5-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="4b5c5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b5c5-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5c5-103">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="4b5c5-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="4b5c5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b5c5-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b5c5-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b5c5-105">DESCRIPTION</span></span>
<span data-ttu-id="4b5c5-106">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="4b5c5-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="4b5c5-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b5c5-107">EXAMPLES</span></span>

### <span data-ttu-id="4b5c5-108">Exemplo 1 remover um IotHub</span><span class="sxs-lookup"><span data-stu-id="4b5c5-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4b5c5-109">Remove um IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="4b5c5-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="4b5c5-110">OS</span><span class="sxs-lookup"><span data-stu-id="4b5c5-110">PARAMETERS</span></span>

### <span data-ttu-id="4b5c5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5c5-111">-DefaultProfile</span></span>
<span data-ttu-id="4b5c5-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4b5c5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b5c5-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b5c5-113">-Name</span></span>
<span data-ttu-id="4b5c5-114">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="4b5c5-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="4b5c5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b5c5-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b5c5-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4b5c5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4b5c5-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4b5c5-117">-Confirm</span></span>
<span data-ttu-id="4b5c5-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b5c5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b5c5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b5c5-119">-WhatIf</span></span>
<span data-ttu-id="4b5c5-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b5c5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b5c5-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b5c5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b5c5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5c5-122">CommonParameters</span></span>
<span data-ttu-id="4b5c5-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b5c5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5c5-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5c5-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5c5-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b5c5-125">INPUTS</span></span>

### <span data-ttu-id="4b5c5-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4b5c5-126">System.String</span></span>

## <span data-ttu-id="4b5c5-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b5c5-127">OUTPUTS</span></span>

### <span data-ttu-id="4b5c5-128">System. void</span><span class="sxs-lookup"><span data-stu-id="4b5c5-128">System.Void</span></span>

## <span data-ttu-id="4b5c5-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b5c5-129">NOTES</span></span>

## <span data-ttu-id="4b5c5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b5c5-130">RELATED LINKS</span></span>
