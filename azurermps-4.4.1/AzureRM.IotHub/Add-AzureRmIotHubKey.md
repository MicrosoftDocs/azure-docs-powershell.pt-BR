---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: f7bbe0c37d03a6db372c6c70da021160060a542a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433117"
---
# <span data-ttu-id="e4873-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e4873-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="e4873-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e4873-102">SYNOPSIS</span></span>
<span data-ttu-id="e4873-103">Cria uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="e4873-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4873-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e4873-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [[-PrimaryKey] <String>] [[-SecondaryKey] <String>] [-Rights] <PSAccessRights>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4873-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e4873-105">DESCRIPTION</span></span>
<span data-ttu-id="e4873-106">Cria uma chave para o IotHub fornecido.</span><span class="sxs-lookup"><span data-stu-id="e4873-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="e4873-107">KeyNames não são exclusivos e precisam ser gerenciados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="e4873-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="e4873-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e4873-108">EXAMPLES</span></span>

### <span data-ttu-id="e4873-109">Exemplo 1 adicionar uma chave a um IotHub</span><span class="sxs-lookup"><span data-stu-id="e4873-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="e4873-110">Cria uma chave chamada "myKey" para o iothub "myiothub" com permissões de RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="e4873-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="e4873-111">OS</span><span class="sxs-lookup"><span data-stu-id="e4873-111">PARAMETERS</span></span>

### <span data-ttu-id="e4873-112">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e4873-112">-KeyName</span></span>
<span data-ttu-id="e4873-113">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="e4873-113">Name of the Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4873-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="e4873-114">-Name</span></span>
<span data-ttu-id="e4873-115">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="e4873-115">Name of the IotHub</span></span>

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

### <span data-ttu-id="e4873-116">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="e4873-116">-PrimaryKey</span></span>
<span data-ttu-id="e4873-117">A chave primária</span><span class="sxs-lookup"><span data-stu-id="e4873-117">The primary key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4873-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4873-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4873-119">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e4873-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e4873-120">-Direitos</span><span class="sxs-lookup"><span data-stu-id="e4873-120">-Rights</span></span>
<span data-ttu-id="e4873-121">As permissões para este IOTHub</span><span class="sxs-lookup"><span data-stu-id="e4873-121">The permissions for this IOTHub</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4873-122">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="e4873-122">-SecondaryKey</span></span>
<span data-ttu-id="e4873-123">A chave secundária</span><span class="sxs-lookup"><span data-stu-id="e4873-123">The Secondary Key</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4873-124">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e4873-124">-Confirm</span></span>
<span data-ttu-id="e4873-125">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4873-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4873-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4873-126">-WhatIf</span></span>
<span data-ttu-id="e4873-127">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e4873-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4873-128">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e4873-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4873-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4873-129">-DefaultProfile</span></span>
<span data-ttu-id="e4873-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e4873-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4873-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4873-131">CommonParameters</span></span>
<span data-ttu-id="e4873-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4873-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4873-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4873-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4873-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e4873-134">INPUTS</span></span>

### <span data-ttu-id="e4873-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e4873-135">System.String</span></span>
<span data-ttu-id="e4873-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="e4873-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="e4873-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e4873-137">OUTPUTS</span></span>

### <span data-ttu-id="e4873-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e4873-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="e4873-139">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="e4873-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="e4873-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e4873-140">NOTES</span></span>

## <span data-ttu-id="e4873-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e4873-141">RELATED LINKS</span></span>

