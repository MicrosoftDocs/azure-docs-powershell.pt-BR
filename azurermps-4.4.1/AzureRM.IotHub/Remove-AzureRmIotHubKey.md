---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 8b7603f145d45411b20b124823f28281d4117127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602220"
---
# <span data-ttu-id="e97a9-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e97a9-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="e97a9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e97a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e97a9-103">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e97a9-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e97a9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e97a9-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e97a9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e97a9-105">DESCRIPTION</span></span>
<span data-ttu-id="e97a9-106">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e97a9-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="e97a9-107">Se houver várias chaves com o mesmo nome que a primeira da lista será removida.</span><span class="sxs-lookup"><span data-stu-id="e97a9-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="e97a9-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e97a9-108">EXAMPLES</span></span>

### <span data-ttu-id="e97a9-109">Exemplo 1 excluir um IotHub</span><span class="sxs-lookup"><span data-stu-id="e97a9-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="e97a9-110">Remove a chave chamada iothubowner1 da IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="e97a9-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="e97a9-111">OS</span><span class="sxs-lookup"><span data-stu-id="e97a9-111">PARAMETERS</span></span>

### <span data-ttu-id="e97a9-112">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e97a9-112">-KeyName</span></span>
<span data-ttu-id="e97a9-113">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="e97a9-113">Name of the Key</span></span>

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

### <span data-ttu-id="e97a9-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e97a9-114">-Name</span></span>
<span data-ttu-id="e97a9-115">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="e97a9-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="e97a9-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e97a9-116">-ResourceGroupName</span></span>
<span data-ttu-id="e97a9-117">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e97a9-117">Resource Group Name</span></span>

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

### <span data-ttu-id="e97a9-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e97a9-118">-Confirm</span></span>
<span data-ttu-id="e97a9-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e97a9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e97a9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e97a9-120">-WhatIf</span></span>
<span data-ttu-id="e97a9-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e97a9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e97a9-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e97a9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e97a9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97a9-123">-DefaultProfile</span></span>
<span data-ttu-id="e97a9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e97a9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e97a9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97a9-125">CommonParameters</span></span>
<span data-ttu-id="e97a9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e97a9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97a9-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e97a9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97a9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e97a9-128">INPUTS</span></span>

### <span data-ttu-id="e97a9-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e97a9-129">System.String</span></span>

## <span data-ttu-id="e97a9-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e97a9-130">OUTPUTS</span></span>

### <span data-ttu-id="e97a9-131">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e97a9-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e97a9-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e97a9-132">NOTES</span></span>

## <span data-ttu-id="e97a9-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e97a9-133">RELATED LINKS</span></span>

