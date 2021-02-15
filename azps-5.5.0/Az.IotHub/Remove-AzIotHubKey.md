---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubKey.md
ms.openlocfilehash: c50ee56a5dcb15c3b199e9aaf08aeca74828cc66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111847"
---
# <span data-ttu-id="7d500-101">Remove-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="7d500-101">Remove-AzIotHubKey</span></span>

## <span data-ttu-id="7d500-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d500-102">SYNOPSIS</span></span>
<span data-ttu-id="7d500-103">Remove uma tecla IotHub.</span><span class="sxs-lookup"><span data-stu-id="7d500-103">Removes an IotHub Key.</span></span>

## <span data-ttu-id="7d500-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d500-104">SYNTAX</span></span>

### <span data-ttu-id="7d500-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7d500-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d500-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d500-106">ResourceIdSet</span></span>
```
Remove-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d500-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7d500-107">DESCRIPTION</span></span>
<span data-ttu-id="7d500-108">Remove uma tecla IotHub.</span><span class="sxs-lookup"><span data-stu-id="7d500-108">Removes an IotHub Key.</span></span>
<span data-ttu-id="7d500-109">Se houver várias teclas com o mesmo nome, a primeira na lista será removida.</span><span class="sxs-lookup"><span data-stu-id="7d500-109">If there are multiple keys with the same name the first one in the list is removed.</span></span>

## <span data-ttu-id="7d500-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7d500-110">EXAMPLES</span></span>

### <span data-ttu-id="7d500-111">Exemplo 1 Excluir um IotHub</span><span class="sxs-lookup"><span data-stu-id="7d500-111">Example 1 Delete an IotHub</span></span>
```
PS C:\> Remove-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "iothubowner1"
```

<span data-ttu-id="7d500-112">Remove a chave chamada iothu bowlner1 do IotHub chamada "myiothub"</span><span class="sxs-lookup"><span data-stu-id="7d500-112">Removes the key named iothubowner1 from the IotHub named "myiothub"</span></span>

## <span data-ttu-id="7d500-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d500-113">PARAMETERS</span></span>

### <span data-ttu-id="7d500-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d500-114">-DefaultProfile</span></span>
<span data-ttu-id="7d500-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="7d500-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d500-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="7d500-116">-HubId</span></span>
<span data-ttu-id="7d500-117">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="7d500-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7d500-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7d500-118">-KeyName</span></span>
<span data-ttu-id="7d500-119">Nome da Chave</span><span class="sxs-lookup"><span data-stu-id="7d500-119">Name of the Key</span></span>

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

### <span data-ttu-id="7d500-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d500-120">-Name</span></span>
<span data-ttu-id="7d500-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="7d500-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="7d500-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d500-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d500-123">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7d500-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7d500-124">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="7d500-124">-Confirm</span></span>
<span data-ttu-id="7d500-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d500-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d500-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d500-126">-WhatIf</span></span>
<span data-ttu-id="7d500-127">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="7d500-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d500-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d500-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d500-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d500-129">CommonParameters</span></span>
<span data-ttu-id="7d500-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d500-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d500-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d500-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d500-132">Entradas</span><span class="sxs-lookup"><span data-stu-id="7d500-132">INPUTS</span></span>

### <span data-ttu-id="7d500-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7d500-133">System.String</span></span>

## <span data-ttu-id="7d500-134">Saídas</span><span class="sxs-lookup"><span data-stu-id="7d500-134">OUTPUTS</span></span>

### <span data-ttu-id="7d500-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d500-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="7d500-136">Notas</span><span class="sxs-lookup"><span data-stu-id="7d500-136">NOTES</span></span>

## <span data-ttu-id="7d500-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d500-137">RELATED LINKS</span></span>
