---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 0f3a6bfa99a199a737c7a69d151d29f5918cc502
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433112"
---
# <span data-ttu-id="0a0b7-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="0a0b7-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="0a0b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0a0b7-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0b7-103">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="0a0b7-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a0b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0a0b7-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a0b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0a0b7-105">DESCRIPTION</span></span>
<span data-ttu-id="0a0b7-106">Exclui um IotHub.</span><span class="sxs-lookup"><span data-stu-id="0a0b7-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="0a0b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0a0b7-107">EXAMPLES</span></span>

### <span data-ttu-id="0a0b7-108">Exemplo 1 remover um IotHub</span><span class="sxs-lookup"><span data-stu-id="0a0b7-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="0a0b7-109">Remove um IotHub chamado "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0a0b7-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="0a0b7-110">OS</span><span class="sxs-lookup"><span data-stu-id="0a0b7-110">PARAMETERS</span></span>

### <span data-ttu-id="0a0b7-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="0a0b7-111">-Name</span></span>
<span data-ttu-id="0a0b7-112">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="0a0b7-112">Name of the IotHub</span></span>

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

### <span data-ttu-id="0a0b7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0b7-113">-ResourceGroupName</span></span>
<span data-ttu-id="0a0b7-114">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0a0b7-114">Resource Group Name</span></span>

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

### <span data-ttu-id="0a0b7-115">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0a0b7-115">-Confirm</span></span>
<span data-ttu-id="0a0b7-116">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a0b7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a0b7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a0b7-117">-WhatIf</span></span>
<span data-ttu-id="0a0b7-118">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0a0b7-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a0b7-119">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0a0b7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a0b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0b7-120">-DefaultProfile</span></span>
<span data-ttu-id="0a0b7-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0b7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a0b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0b7-122">CommonParameters</span></span>
<span data-ttu-id="0a0b7-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a0b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0b7-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a0b7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0b7-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0a0b7-125">INPUTS</span></span>

### <span data-ttu-id="0a0b7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="0a0b7-126">System.String</span></span>

## <span data-ttu-id="0a0b7-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0a0b7-127">OUTPUTS</span></span>

### <span data-ttu-id="0a0b7-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="0a0b7-128">System.Object</span></span>

## <span data-ttu-id="0a0b7-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0a0b7-129">NOTES</span></span>

## <span data-ttu-id="0a0b7-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0a0b7-130">RELATED LINKS</span></span>

