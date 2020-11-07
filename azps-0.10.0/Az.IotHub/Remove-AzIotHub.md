---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Remove-AzIotHub.md
ms.openlocfilehash: 0e83ec5266bc807f64bd231a3a423ad8cc7db190
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776686"
---
# <span data-ttu-id="a6614-101">Remove-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="a6614-101">Remove-AzIotHub</span></span>

## <span data-ttu-id="a6614-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a6614-102">SYNOPSIS</span></span>
<span data-ttu-id="a6614-103">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="a6614-103">Deletes an IotHub.</span></span>

## <span data-ttu-id="a6614-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a6614-104">SYNTAX</span></span>

```
Remove-AzIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6614-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a6614-105">DESCRIPTION</span></span>
<span data-ttu-id="a6614-106">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="a6614-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="a6614-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a6614-107">EXAMPLES</span></span>

### <span data-ttu-id="a6614-108">Exemplo 1 remover um IotHub</span><span class="sxs-lookup"><span data-stu-id="a6614-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="a6614-109">Remove um IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="a6614-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="a6614-110">OS</span><span class="sxs-lookup"><span data-stu-id="a6614-110">PARAMETERS</span></span>

### <span data-ttu-id="a6614-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6614-111">-DefaultProfile</span></span>
<span data-ttu-id="a6614-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a6614-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6614-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a6614-113">-Name</span></span>
<span data-ttu-id="a6614-114">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="a6614-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="a6614-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6614-115">-ResourceGroupName</span></span>
<span data-ttu-id="a6614-116">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="a6614-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a6614-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a6614-117">-Confirm</span></span>
<span data-ttu-id="a6614-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6614-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6614-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6614-119">-WhatIf</span></span>
<span data-ttu-id="a6614-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a6614-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6614-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a6614-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6614-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6614-122">CommonParameters</span></span>
<span data-ttu-id="a6614-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6614-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6614-124">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6614-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6614-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a6614-125">INPUTS</span></span>

### <span data-ttu-id="a6614-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a6614-126">System.String</span></span>

## <span data-ttu-id="a6614-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a6614-127">OUTPUTS</span></span>

### <span data-ttu-id="a6614-128">System. void</span><span class="sxs-lookup"><span data-stu-id="a6614-128">System.Void</span></span>

## <span data-ttu-id="a6614-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a6614-129">NOTES</span></span>

## <span data-ttu-id="a6614-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a6614-130">RELATED LINKS</span></span>
