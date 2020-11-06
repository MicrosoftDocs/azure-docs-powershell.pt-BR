---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 0f48bf7ad03dcfd59f8ea3653acdb7a57aa5240c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428112"
---
# <span data-ttu-id="5ab42-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="5ab42-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="5ab42-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5ab42-102">SYNOPSIS</span></span>
<span data-ttu-id="5ab42-103">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="5ab42-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ab42-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5ab42-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ab42-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5ab42-105">DESCRIPTION</span></span>
<span data-ttu-id="5ab42-106">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="5ab42-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="5ab42-107">Se houver várias chaves com o mesmo nome que a primeira da lista será removida.</span><span class="sxs-lookup"><span data-stu-id="5ab42-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="5ab42-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5ab42-108">EXAMPLES</span></span>

### <span data-ttu-id="5ab42-109">Exemplo 1 excluir um IotHub</span><span class="sxs-lookup"><span data-stu-id="5ab42-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="5ab42-110">Remove a chave chamada iothubowner1 da IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5ab42-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5ab42-111">OS</span><span class="sxs-lookup"><span data-stu-id="5ab42-111">PARAMETERS</span></span>

### <span data-ttu-id="5ab42-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ab42-112">-DefaultProfile</span></span>
<span data-ttu-id="5ab42-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5ab42-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ab42-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="5ab42-114">-KeyName</span></span>
<span data-ttu-id="5ab42-115">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="5ab42-115">Name of the Key</span></span>

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

### <span data-ttu-id="5ab42-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5ab42-116">-Name</span></span>
<span data-ttu-id="5ab42-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="5ab42-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="5ab42-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ab42-118">-ResourceGroupName</span></span>
<span data-ttu-id="5ab42-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5ab42-119">Resource Group Name</span></span>

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

### <span data-ttu-id="5ab42-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5ab42-120">-Confirm</span></span>
<span data-ttu-id="5ab42-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ab42-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ab42-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ab42-122">-WhatIf</span></span>
<span data-ttu-id="5ab42-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5ab42-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ab42-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5ab42-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ab42-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ab42-125">CommonParameters</span></span>
<span data-ttu-id="5ab42-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ab42-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ab42-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ab42-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ab42-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5ab42-128">INPUTS</span></span>

### <span data-ttu-id="5ab42-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5ab42-129">System.String</span></span>

## <span data-ttu-id="5ab42-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5ab42-130">OUTPUTS</span></span>

### <span data-ttu-id="5ab42-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ab42-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="5ab42-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5ab42-132">NOTES</span></span>

## <span data-ttu-id="5ab42-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5ab42-133">RELATED LINKS</span></span>
