---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: 7dd27544e3304570cf3fbdae861b21eabd300c35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887508"
---
# <span data-ttu-id="1f7f7-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="1f7f7-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="1f7f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7f7-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7f7-103">Gere uma chave do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="1f7f7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1f7f7-104">SYNTAX</span></span>

### <span data-ttu-id="1f7f7-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f7f7-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f7f7-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1f7f7-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f7f7-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1f7f7-107">DESCRIPTION</span></span>
<span data-ttu-id="1f7f7-108">Gere uma chave do Hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="1f7f7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f7f7-109">EXAMPLES</span></span>

### <span data-ttu-id="1f7f7-110">Exemplo 1 Regenerar chave primária</span><span class="sxs-lookup"><span data-stu-id="1f7f7-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="1f7f7-111">Chave primária regenerada para a política de autorização "testKey" de um hub de iot do azure.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="1f7f7-112">Exemplo 2 Teclas de troca</span><span class="sxs-lookup"><span data-stu-id="1f7f7-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="1f7f7-113">Trocar chaves pela política de autorização "testKey" de um hub de iot do azure.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="1f7f7-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1f7f7-114">PARAMETERS</span></span>

### <span data-ttu-id="1f7f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f7f7-115">-DefaultProfile</span></span>
<span data-ttu-id="1f7f7-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1f7f7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f7f7-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="1f7f7-117">-HubId</span></span>
<span data-ttu-id="1f7f7-118">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="1f7f7-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="1f7f7-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1f7f7-119">-KeyName</span></span>
<span data-ttu-id="1f7f7-120">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="1f7f7-120">Name of the Key</span></span>

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

### <span data-ttu-id="1f7f7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1f7f7-121">-Name</span></span>
<span data-ttu-id="1f7f7-122">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="1f7f7-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="1f7f7-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="1f7f7-123">-RenewKey</span></span>
<span data-ttu-id="1f7f7-124">Tecla Regenerar.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="1f7f7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f7f7-125">-ResourceGroupName</span></span>
<span data-ttu-id="1f7f7-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="1f7f7-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1f7f7-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f7f7-127">-Confirm</span></span>
<span data-ttu-id="1f7f7-128">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f7f7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f7f7-129">-WhatIf</span></span>
<span data-ttu-id="1f7f7-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f7f7-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f7f7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7f7-132">CommonParameters</span></span>
<span data-ttu-id="1f7f7-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7f7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7f7-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7f7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7f7-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f7f7-135">INPUTS</span></span>

### <span data-ttu-id="1f7f7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1f7f7-136">System.String</span></span>

## <span data-ttu-id="1f7f7-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1f7f7-137">OUTPUTS</span></span>

### <span data-ttu-id="1f7f7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="1f7f7-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="1f7f7-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="1f7f7-139">NOTES</span></span>

## <span data-ttu-id="1f7f7-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f7f7-140">RELATED LINKS</span></span>
