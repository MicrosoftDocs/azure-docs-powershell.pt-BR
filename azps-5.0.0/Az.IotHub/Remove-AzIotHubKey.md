---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115323"
---
# <span data-ttu-id="0db11-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="0db11-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="0db11-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0db11-102">SYNOPSIS</span></span>
<span data-ttu-id="0db11-103">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="0db11-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="0db11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0db11-104">SYNTAX</span></span>

### <span data-ttu-id="0db11-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="0db11-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db11-106">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="0db11-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0db11-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0db11-107">DESCRIPTION</span></span>
<span data-ttu-id="0db11-108">Remove uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="0db11-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="0db11-109">Se houver várias chaves com o mesmo nome que a primeira da lista será removida.</span><span class="sxs-lookup"><span data-stu-id="0db11-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="0db11-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0db11-110">EXAMPLES</span></span>

### <span data-ttu-id="0db11-111">Exemplo 1 excluir um IotHub</span><span class="sxs-lookup"><span data-stu-id="0db11-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="0db11-112">Remove a chave chamada iothubowner1 da IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="0db11-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="0db11-113">OS</span><span class="sxs-lookup"><span data-stu-id="0db11-113">PARAMETERS</span></span>

### <span data-ttu-id="0db11-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db11-114">-DefaultProfile</span></span>
<span data-ttu-id="0db11-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="0db11-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0db11-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="0db11-116">-HubId</span></span>
<span data-ttu-id="0db11-117">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="0db11-117">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0db11-118">-KeyName</span></span>
<span data-ttu-id="0db11-119">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="0db11-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0db11-120">-Name</span></span>
<span data-ttu-id="0db11-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="0db11-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db11-122">-ResourceGroupName</span></span>
<span data-ttu-id="0db11-123">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="0db11-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0db11-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="0db11-124">-Confirm</span></span>
<span data-ttu-id="0db11-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0db11-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db11-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db11-126">-WhatIf</span></span>
<span data-ttu-id="0db11-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="0db11-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db11-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0db11-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db11-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db11-129">CommonParameters</span></span>
<span data-ttu-id="0db11-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db11-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db11-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db11-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db11-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0db11-132">INPUTS</span></span>

### <span data-ttu-id="0db11-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0db11-133">System.String</span></span>

## <span data-ttu-id="0db11-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0db11-134">OUTPUTS</span></span>

### <span data-ttu-id="0db11-135">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0db11-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="0db11-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0db11-136">NOTES</span></span>

## <span data-ttu-id="0db11-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0db11-137">RELATED LINKS</span></span>
