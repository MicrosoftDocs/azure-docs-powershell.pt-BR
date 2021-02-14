---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116743"
---
# <span data-ttu-id="36917-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="36917-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="36917-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36917-102">SYNOPSIS</span></span>
<span data-ttu-id="36917-103">Gere uma tecla hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="36917-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="36917-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36917-104">SYNTAX</span></span>

### <span data-ttu-id="36917-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36917-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36917-106">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36917-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36917-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="36917-107">DESCRIPTION</span></span>
<span data-ttu-id="36917-108">Gere uma tecla hub do Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="36917-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="36917-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36917-109">EXAMPLES</span></span>

### <span data-ttu-id="36917-110">Exemplo 1 Regenerar chave primária</span><span class="sxs-lookup"><span data-stu-id="36917-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="36917-111">Chave primária regenerada para a política de autorização "testKey" de um hub do azure iot.</span><span class="sxs-lookup"><span data-stu-id="36917-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="36917-112">Exemplo 2 Teclas de troca</span><span class="sxs-lookup"><span data-stu-id="36917-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="36917-113">Trocar chaves para a política de autorização "testKey" de um hub do azure iot.</span><span class="sxs-lookup"><span data-stu-id="36917-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="36917-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36917-114">PARAMETERS</span></span>

### <span data-ttu-id="36917-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36917-115">-DefaultProfile</span></span>
<span data-ttu-id="36917-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="36917-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36917-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="36917-117">-HubId</span></span>
<span data-ttu-id="36917-118">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="36917-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="36917-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="36917-119">-KeyName</span></span>
<span data-ttu-id="36917-120">Nome da Chave</span><span class="sxs-lookup"><span data-stu-id="36917-120">Name of the Key</span></span>

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

### <span data-ttu-id="36917-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="36917-121">-Name</span></span>
<span data-ttu-id="36917-122">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="36917-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="36917-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="36917-123">-RenewKey</span></span>
<span data-ttu-id="36917-124">Regenerar a chave.</span><span class="sxs-lookup"><span data-stu-id="36917-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="36917-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36917-125">-ResourceGroupName</span></span>
<span data-ttu-id="36917-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="36917-126">Resource Group Name</span></span>

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

### <span data-ttu-id="36917-127">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="36917-127">-Confirm</span></span>
<span data-ttu-id="36917-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36917-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36917-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36917-129">-WhatIf</span></span>
<span data-ttu-id="36917-130">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="36917-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36917-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="36917-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36917-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36917-132">CommonParameters</span></span>
<span data-ttu-id="36917-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36917-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36917-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36917-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36917-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="36917-135">INPUTS</span></span>

### <span data-ttu-id="36917-136">System.String</span><span class="sxs-lookup"><span data-stu-id="36917-136">System.String</span></span>

## <span data-ttu-id="36917-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="36917-137">OUTPUTS</span></span>

### <span data-ttu-id="36917-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36917-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="36917-139">Notas</span><span class="sxs-lookup"><span data-stu-id="36917-139">NOTES</span></span>

## <span data-ttu-id="36917-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36917-140">RELATED LINKS</span></span>
