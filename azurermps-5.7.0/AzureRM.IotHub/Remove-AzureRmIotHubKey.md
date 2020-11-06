---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHubKey.md
ms.openlocfilehash: 4f1c21f4f64193ec25a0392e094b8fd492ceba9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429768"
---
# <span data-ttu-id="f931b-101">Remove-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="f931b-101">Remove-AzureRmIotHubKey</span></span>

## <span data-ttu-id="f931b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f931b-102">SYNOPSIS</span></span>
<span data-ttu-id="f931b-103">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="f931b-103">Removes an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f931b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f931b-104">SYNTAX</span></span>

```
Remove-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f931b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f931b-105">DESCRIPTION</span></span>
<span data-ttu-id="f931b-106">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="f931b-106">Removes an IotHub Key.</span></span>
<span data-ttu-id="f931b-107">Se houver várias chaves com o mesmo nome que a primeira da lista será removida.</span><span class="sxs-lookup"><span data-stu-id="f931b-107">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="f931b-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f931b-108">EXAMPLES</span></span>

### <span data-ttu-id="f931b-109">Exemplo 1 excluir um IotHub</span><span class="sxs-lookup"><span data-stu-id="f931b-109">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="f931b-110">Remove a chave chamada iothubowner1 da IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="f931b-110">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="f931b-111">OS</span><span class="sxs-lookup"><span data-stu-id="f931b-111">PARAMETERS</span></span>

### <span data-ttu-id="f931b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f931b-112">-DefaultProfile</span></span>
<span data-ttu-id="f931b-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f931b-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f931b-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f931b-114">-KeyName</span></span>
<span data-ttu-id="f931b-115">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="f931b-115">Name of the Key</span></span>

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

### <span data-ttu-id="f931b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f931b-116">-Name</span></span>
<span data-ttu-id="f931b-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="f931b-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="f931b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f931b-118">-ResourceGroupName</span></span>
<span data-ttu-id="f931b-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f931b-119">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f931b-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f931b-120">-Confirm</span></span>
<span data-ttu-id="f931b-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f931b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f931b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f931b-122">-WhatIf</span></span>
<span data-ttu-id="f931b-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f931b-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f931b-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f931b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f931b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f931b-125">CommonParameters</span></span>
<span data-ttu-id="f931b-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f931b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f931b-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f931b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f931b-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f931b-128">INPUTS</span></span>

### <span data-ttu-id="f931b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f931b-129">System.String</span></span>

## <span data-ttu-id="f931b-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f931b-130">OUTPUTS</span></span>

### <span data-ttu-id="f931b-131">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f931b-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f931b-132">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f931b-132">NOTES</span></span>

## <span data-ttu-id="f931b-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f931b-133">RELATED LINKS</span></span>

