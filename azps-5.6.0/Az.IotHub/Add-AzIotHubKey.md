---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: fe964ba2672c67fc9bb5e47e7b7a16d4fdd49471
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891358"
---
# <span data-ttu-id="fa5cb-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="fa5cb-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="fa5cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa5cb-102">SYNOPSIS</span></span>
<span data-ttu-id="fa5cb-103">Cria uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="fa5cb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="fa5cb-104">SYNTAX</span></span>

### <span data-ttu-id="fa5cb-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="fa5cb-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa5cb-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fa5cb-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa5cb-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="fa5cb-107">DESCRIPTION</span></span>
<span data-ttu-id="fa5cb-108">Cria uma chave para o IotHub fornecido.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="fa5cb-109">KeyNames não são exclusivos e precisam ser gerenciados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="fa5cb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa5cb-110">EXAMPLES</span></span>

### <span data-ttu-id="fa5cb-111">Exemplo 1 Adicionar uma chave a um IotHub</span><span class="sxs-lookup"><span data-stu-id="fa5cb-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="fa5cb-112">Cria uma chave chamada "mykey" para o iothub "myiothub" com permissões registryRead.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="fa5cb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="fa5cb-113">PARAMETERS</span></span>

### <span data-ttu-id="fa5cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa5cb-114">-DefaultProfile</span></span>
<span data-ttu-id="fa5cb-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="fa5cb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa5cb-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="fa5cb-116">-HubId</span></span>
<span data-ttu-id="fa5cb-117">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="fa5cb-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fa5cb-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="fa5cb-118">-KeyName</span></span>
<span data-ttu-id="fa5cb-119">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="fa5cb-119">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5cb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fa5cb-120">-Name</span></span>
<span data-ttu-id="fa5cb-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="fa5cb-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="fa5cb-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="fa5cb-122">-PrimaryKey</span></span>
<span data-ttu-id="fa5cb-123">A chave primária</span><span class="sxs-lookup"><span data-stu-id="fa5cb-123">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5cb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa5cb-124">-ResourceGroupName</span></span>
<span data-ttu-id="fa5cb-125">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="fa5cb-125">Resource Group Name</span></span>

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

### <span data-ttu-id="fa5cb-126">-Rights</span><span class="sxs-lookup"><span data-stu-id="fa5cb-126">-Rights</span></span>
<span data-ttu-id="fa5cb-127">As permissões para este IOTHub</span><span class="sxs-lookup"><span data-stu-id="fa5cb-127">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases:
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5cb-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="fa5cb-128">-SecondaryKey</span></span>
<span data-ttu-id="fa5cb-129">A chave secundária</span><span class="sxs-lookup"><span data-stu-id="fa5cb-129">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa5cb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa5cb-130">-Confirm</span></span>
<span data-ttu-id="fa5cb-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa5cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa5cb-132">-WhatIf</span></span>
<span data-ttu-id="fa5cb-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa5cb-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa5cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa5cb-135">CommonParameters</span></span>
<span data-ttu-id="fa5cb-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa5cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa5cb-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa5cb-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa5cb-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa5cb-138">INPUTS</span></span>

### <span data-ttu-id="fa5cb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="fa5cb-139">System.String</span></span>

## <span data-ttu-id="fa5cb-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="fa5cb-140">OUTPUTS</span></span>

### <span data-ttu-id="fa5cb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fa5cb-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="fa5cb-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="fa5cb-142">NOTES</span></span>

## <span data-ttu-id="fa5cb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa5cb-143">RELATED LINKS</span></span>
