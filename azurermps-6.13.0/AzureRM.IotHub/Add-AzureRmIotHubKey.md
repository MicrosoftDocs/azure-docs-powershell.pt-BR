---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/add-azurermiothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Add-AzureRmIotHubKey.md
ms.openlocfilehash: 379aaa360776291515f1848cd48b24e88be23ef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430243"
---
# <span data-ttu-id="be555-101">Add-AzureRmIotHubKey</span><span class="sxs-lookup"><span data-stu-id="be555-101">Add-AzureRmIotHubKey</span></span>

## <span data-ttu-id="be555-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="be555-102">SYNOPSIS</span></span>
<span data-ttu-id="be555-103">Cria uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="be555-103">Creates an IotHub Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be555-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="be555-104">SYNTAX</span></span>

```
Add-AzureRmIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be555-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="be555-105">DESCRIPTION</span></span>
<span data-ttu-id="be555-106">Cria uma chave para o IotHub fornecido.</span><span class="sxs-lookup"><span data-stu-id="be555-106">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="be555-107">KeyNames não são exclusivos e precisam ser gerenciados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="be555-107">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="be555-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="be555-108">EXAMPLES</span></span>

### <span data-ttu-id="be555-109">Exemplo 1 adicionar uma chave a um IotHub</span><span class="sxs-lookup"><span data-stu-id="be555-109">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzureRmIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="be555-110">Cria uma chave chamada "myKey" para o iothub "myiothub" com permissões de RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="be555-110">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="be555-111">OS</span><span class="sxs-lookup"><span data-stu-id="be555-111">PARAMETERS</span></span>

### <span data-ttu-id="be555-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be555-112">-DefaultProfile</span></span>
<span data-ttu-id="be555-113">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="be555-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be555-114">-KeyName</span><span class="sxs-lookup"><span data-stu-id="be555-114">-KeyName</span></span>
<span data-ttu-id="be555-115">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="be555-115">Name of the Key</span></span>

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

### <span data-ttu-id="be555-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="be555-116">-Name</span></span>
<span data-ttu-id="be555-117">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="be555-117">Name of the IotHub</span></span>

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

### <span data-ttu-id="be555-118">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="be555-118">-PrimaryKey</span></span>
<span data-ttu-id="be555-119">A chave primária</span><span class="sxs-lookup"><span data-stu-id="be555-119">The primary key</span></span>

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

### <span data-ttu-id="be555-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be555-120">-ResourceGroupName</span></span>
<span data-ttu-id="be555-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="be555-121">Resource Group Name</span></span>

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

### <span data-ttu-id="be555-122">-Direitos</span><span class="sxs-lookup"><span data-stu-id="be555-122">-Rights</span></span>
<span data-ttu-id="be555-123">As permissões para este IOTHub</span><span class="sxs-lookup"><span data-stu-id="be555-123">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="be555-124">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="be555-124">-SecondaryKey</span></span>
<span data-ttu-id="be555-125">A chave secundária</span><span class="sxs-lookup"><span data-stu-id="be555-125">The Secondary Key</span></span>

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

### <span data-ttu-id="be555-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="be555-126">-Confirm</span></span>
<span data-ttu-id="be555-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be555-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be555-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be555-128">-WhatIf</span></span>
<span data-ttu-id="be555-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="be555-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be555-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="be555-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be555-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be555-131">CommonParameters</span></span>
<span data-ttu-id="be555-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be555-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be555-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be555-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be555-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="be555-134">INPUTS</span></span>

### <span data-ttu-id="be555-135">System. String</span><span class="sxs-lookup"><span data-stu-id="be555-135">System.String</span></span>

## <span data-ttu-id="be555-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="be555-136">OUTPUTS</span></span>

### <span data-ttu-id="be555-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="be555-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="be555-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="be555-138">NOTES</span></span>

## <span data-ttu-id="be555-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="be555-139">RELATED LINKS</span></span>
