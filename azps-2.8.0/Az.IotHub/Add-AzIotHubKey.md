---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubKey.md
ms.openlocfilehash: 3505a2b18ac35644fe401dea4aca8c96b10a7f2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596295"
---
# <span data-ttu-id="b0640-101">Add-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="b0640-101">Add-AzIotHubKey</span></span>

## <span data-ttu-id="b0640-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b0640-102">SYNOPSIS</span></span>
<span data-ttu-id="b0640-103">Cria uma chave IotHub.</span><span class="sxs-lookup"><span data-stu-id="b0640-103">Creates an IotHub Key.</span></span>

## <span data-ttu-id="b0640-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0640-104">SYNTAX</span></span>

### <span data-ttu-id="b0640-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b0640-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-PrimaryKey <String>]
 [-SecondaryKey <String>] -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0640-106">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="b0640-106">ResourceIdSet</span></span>
```
Add-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 -Rights <PSAccessRights> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0640-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b0640-107">DESCRIPTION</span></span>
<span data-ttu-id="b0640-108">Cria uma chave para o IotHub fornecido.</span><span class="sxs-lookup"><span data-stu-id="b0640-108">Creates a Key for the provided IotHub.</span></span>
<span data-ttu-id="b0640-109">KeyNames não são exclusivos e precisam ser gerenciados com cuidado.</span><span class="sxs-lookup"><span data-stu-id="b0640-109">KeyNames are not unique and need to be managed carefully.</span></span>

## <span data-ttu-id="b0640-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b0640-110">EXAMPLES</span></span>

### <span data-ttu-id="b0640-111">Exemplo 1 adicionar uma chave a um IotHub</span><span class="sxs-lookup"><span data-stu-id="b0640-111">Example 1 Add a Key to an IotHub</span></span>
```
PS C:\> Add-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "newkey" -PrimaryKey "primarykey" -SecondaryKey "secondarykey" -Rights RegistryRead
```

<span data-ttu-id="b0640-112">Cria uma chave chamada "myKey" para o iothub "myiothub" com permissões de RegistryRead.</span><span class="sxs-lookup"><span data-stu-id="b0640-112">Creates a key named "mykey" for the iothub "myiothub" with RegistryRead permissions.</span></span>

## <span data-ttu-id="b0640-113">OS</span><span class="sxs-lookup"><span data-stu-id="b0640-113">PARAMETERS</span></span>

### <span data-ttu-id="b0640-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0640-114">-DefaultProfile</span></span>
<span data-ttu-id="b0640-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b0640-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0640-116">-HubId</span><span class="sxs-lookup"><span data-stu-id="b0640-116">-HubId</span></span>
<span data-ttu-id="b0640-117">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="b0640-117">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b0640-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b0640-118">-KeyName</span></span>
<span data-ttu-id="b0640-119">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="b0640-119">Name of the Key</span></span>

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

### <span data-ttu-id="b0640-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0640-120">-Name</span></span>
<span data-ttu-id="b0640-121">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="b0640-121">Name of the IotHub</span></span>

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

### <span data-ttu-id="b0640-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b0640-122">-PrimaryKey</span></span>
<span data-ttu-id="b0640-123">A chave primária</span><span class="sxs-lookup"><span data-stu-id="b0640-123">The primary key</span></span>

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

### <span data-ttu-id="b0640-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0640-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0640-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b0640-125">Resource Group Name</span></span>

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

### <span data-ttu-id="b0640-126">-Direitos</span><span class="sxs-lookup"><span data-stu-id="b0640-126">-Rights</span></span>
<span data-ttu-id="b0640-127">As permissões para este IOTHub</span><span class="sxs-lookup"><span data-stu-id="b0640-127">The permissions for this IOTHub</span></span>

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

### <span data-ttu-id="b0640-128">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="b0640-128">-SecondaryKey</span></span>
<span data-ttu-id="b0640-129">A chave secundária</span><span class="sxs-lookup"><span data-stu-id="b0640-129">The Secondary Key</span></span>

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

### <span data-ttu-id="b0640-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b0640-130">-Confirm</span></span>
<span data-ttu-id="b0640-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0640-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0640-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0640-132">-WhatIf</span></span>
<span data-ttu-id="b0640-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b0640-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0640-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b0640-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0640-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0640-135">CommonParameters</span></span>
<span data-ttu-id="b0640-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0640-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0640-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0640-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0640-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b0640-138">INPUTS</span></span>

### <span data-ttu-id="b0640-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b0640-139">System.String</span></span>

## <span data-ttu-id="b0640-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b0640-140">OUTPUTS</span></span>

### <span data-ttu-id="b0640-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b0640-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="b0640-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b0640-142">NOTES</span></span>

## <span data-ttu-id="b0640-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b0640-143">RELATED LINKS</span></span>
