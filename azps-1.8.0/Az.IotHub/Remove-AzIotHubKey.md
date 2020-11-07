---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c275ac087c24c58de73e72ac5dcf46839d710621
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770700"
---
# <span data-ttu-id="e3f34-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e3f34-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="e3f34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e3f34-102">SYNOPSIS</span></span>
<span data-ttu-id="e3f34-103">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e3f34-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="e3f34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3f34-104">SYNTAX</span></span>

```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3f34-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e3f34-105">DESCRIPTION</span></span>
<span data-ttu-id="e3f34-106">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e3f34-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="e3f34-107">Se houver várias chaves com o mesmo nome que a primeira da lista será removida.</span><span class="sxs-lookup"><span data-stu-id="e3f34-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="e3f34-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3f34-108">EXAMPLES</span></span>

### <span data-ttu-id="e3f34-109">Exemplo 1 excluir um IotHub</span><span class="sxs-lookup"><span data-stu-id="e3f34-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="e3f34-110">Remove a chave chamada iothubowner1 da IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e3f34-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e3f34-111">OS</span><span class="sxs-lookup"><span data-stu-id="e3f34-111">PARAMETERS</span></span>

### <span data-ttu-id="e3f34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3f34-112">-DefaultProfile</span></span>
<span data-ttu-id="e3f34-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e3f34-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e3f34-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e3f34-114">-KeyName</span></span>
<span data-ttu-id="e3f34-115">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="e3f34-115">Name of the Key</span></span>

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

### <span data-ttu-id="e3f34-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3f34-116">-Name</span></span>
<span data-ttu-id="e3f34-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="e3f34-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="e3f34-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3f34-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3f34-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e3f34-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e3f34-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e3f34-120">-Confirm</span></span>
<span data-ttu-id="e3f34-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3f34-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3f34-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3f34-122">-WhatIf</span></span>
<span data-ttu-id="e3f34-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3f34-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3f34-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3f34-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3f34-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3f34-125">CommonParameters</span></span>
<span data-ttu-id="e3f34-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3f34-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3f34-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3f34-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3f34-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e3f34-128">INPUTS</span></span>

### <span data-ttu-id="e3f34-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e3f34-129">System.String</span></span>

## <span data-ttu-id="e3f34-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e3f34-130">OUTPUTS</span></span>

### <span data-ttu-id="e3f34-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e3f34-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e3f34-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e3f34-132">NOTES</span></span>

## <span data-ttu-id="e3f34-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3f34-133">RELATED LINKS</span></span>
