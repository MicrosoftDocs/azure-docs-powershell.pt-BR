---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: c56b147c5ac62e376eff1159eb679c5a692eb1b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431679"
---
# <span data-ttu-id="7d84f-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="7d84f-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="7d84f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7d84f-102">SYNOPSIS</span></span>
<span data-ttu-id="7d84f-103">Cria uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="7d84f-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d84f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7d84f-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d84f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7d84f-105">DESCRIPTION</span></span>
<span data-ttu-id="7d84f-106">Cria uma chave para o IotHub fornecido.</span><span class="sxs-lookup"><span data-stu-id="7d84f-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="7d84f-107">KeyNames não são exclusivos e precisam ser gerenciados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="7d84f-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="7d84f-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7d84f-108">EXAMPLES</span></span>

### <span data-ttu-id="7d84f-109">Exemplo 1 adicionar uma chave a um IotHub</span><span class="sxs-lookup"><span data-stu-id="7d84f-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="7d84f-110">Cria uma chave chamada "myKey" para o iothub "myiothub" com permissões de RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="7d84f-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="7d84f-111">OS</span><span class="sxs-lookup"><span data-stu-id="7d84f-111">PARAMETERS</span></span>

### <span data-ttu-id="7d84f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d84f-112">-DefaultProfile</span></span>
<span data-ttu-id="7d84f-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7d84f-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d84f-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7d84f-114">-KeyName</span></span>
<span data-ttu-id="7d84f-115">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="7d84f-115">Name of the Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d84f-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d84f-116">-Name</span></span>
<span data-ttu-id="7d84f-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="7d84f-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="7d84f-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7d84f-118">-PrimaryKey</span></span>
<span data-ttu-id="7d84f-119">A chave primária</span><span class="sxs-lookup"><span data-stu-id="7d84f-119">The primary key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d84f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d84f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d84f-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7d84f-121">Resource Group Name</span></span>

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

### <span data-ttu-id="7d84f-122">-Direitos</span><span class="sxs-lookup"><span data-stu-id="7d84f-122">-Rights</span></span>
<span data-ttu-id="7d84f-123">As permissões para este IOTHub</span><span class="sxs-lookup"><span data-stu-id="7d84f-123">The permissions for this IOTHub</span></span>

```yaml
Type: PSAccessRights
Parameter Sets: (All)
Aliases: 
Accepted values: RegistryRead, RegistryWrite, ServiceConnect, DeviceConnect

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d84f-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="7d84f-124">-SecondaryKey</span></span>
<span data-ttu-id="7d84f-125">A chave secundária</span><span class="sxs-lookup"><span data-stu-id="7d84f-125">The Secondary Key</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d84f-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7d84f-126">-Confirm</span></span>
<span data-ttu-id="7d84f-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d84f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d84f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d84f-128">-WhatIf</span></span>
<span data-ttu-id="7d84f-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7d84f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d84f-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7d84f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d84f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d84f-131">CommonParameters</span></span>
<span data-ttu-id="7d84f-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d84f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d84f-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d84f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d84f-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7d84f-134">INPUTS</span></span>

### <span data-ttu-id="7d84f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7d84f-135">System.String</span></span>
<span data-ttu-id="7d84f-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSAccessRights</span><span class="sxs-lookup"><span data-stu-id="7d84f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSAccessRights</span></span>

## <span data-ttu-id="7d84f-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7d84f-137">OUTPUTS</span></span>

### <span data-ttu-id="7d84f-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7d84f-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>
<span data-ttu-id="7d84f-139">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="7d84f-139">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="7d84f-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7d84f-140">NOTES</span></span>

## <span data-ttu-id="7d84f-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7d84f-141">RELATED LINKS</span></span>

