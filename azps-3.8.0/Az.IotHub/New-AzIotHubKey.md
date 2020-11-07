---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubKey.md
ms.openlocfilehash: cc843ca942ae79fe76e1dd50e76c876e4d05b5ac
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943805"
---
# <span data-ttu-id="e08d2-101">New-AzIotHubKey</span><span class="sxs-lookup"><span data-stu-id="e08d2-101">New-AzIotHubKey</span></span>

## <span data-ttu-id="e08d2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e08d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e08d2-103">Gerar uma chave do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="e08d2-103">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="e08d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e08d2-104">SYNTAX</span></span>

### <span data-ttu-id="e08d2-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="e08d2-105">ResourceSet (Default)</span></span>
```
New-AzIotHubKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08d2-106">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="e08d2-106">ResourceIdSet</span></span>
```
New-AzIotHubKey [-HubId] <String> [-KeyName] <String> [-RenewKey] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08d2-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e08d2-107">DESCRIPTION</span></span>
<span data-ttu-id="e08d2-108">Gerar uma chave do Hub IoT do Azure.</span><span class="sxs-lookup"><span data-stu-id="e08d2-108">Generate an Azure IoT Hub key.</span></span>

## <span data-ttu-id="e08d2-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e08d2-109">EXAMPLES</span></span>

### <span data-ttu-id="e08d2-110">Exemplo 1 gerar novamente a chave primária</span><span class="sxs-lookup"><span data-stu-id="e08d2-110">Example 1 Regenerate primary key</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "primary"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=    6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=        ServiceConnect
```

<span data-ttu-id="e08d2-111">Chave primária regenerada para a política de autorização "testKey" de um hub IOT do Azure.</span><span class="sxs-lookup"><span data-stu-id="e08d2-111">Regenerated primary key for the authorization policy "testKey" of an azure iot hub.</span></span>

### <span data-ttu-id="e08d2-112">Exemplo 2 teclas de permuta</span><span class="sxs-lookup"><span data-stu-id="e08d2-112">Example 2 Swapping keys</span></span>
```
PS C:\> New-AzIotHubKey -ResourceGroupName "myresourcegroup" -Name "myiothub" -KeyName "testKey" -RenewKey "swap"

KeyName     PrimaryKey                                      SecondaryKey                                        Rights
-------     ----------                                      ------------                                        ------
test        6JqGKGUTL0mhQwvcOeIRT7OnT6noK/tie6jBY77sJTE=    SXSdm31aT+i3939xSnA191f8g3uRhIUCTsO26b9s/nE=        ServiceConnect
```

<span data-ttu-id="e08d2-113">Chaves de troca da política de autorização "testKey" de um hub IOT do Azure.</span><span class="sxs-lookup"><span data-stu-id="e08d2-113">Swapping keys for the authorization policy "testKey" of an azure iot hub.</span></span>

## <span data-ttu-id="e08d2-114">OS</span><span class="sxs-lookup"><span data-stu-id="e08d2-114">PARAMETERS</span></span>

### <span data-ttu-id="e08d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e08d2-115">-DefaultProfile</span></span>
<span data-ttu-id="e08d2-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e08d2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e08d2-117">-HubId</span><span class="sxs-lookup"><span data-stu-id="e08d2-117">-HubId</span></span>
<span data-ttu-id="e08d2-118">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="e08d2-118">IotHub Resource Id</span></span>

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

### <span data-ttu-id="e08d2-119">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e08d2-119">-KeyName</span></span>
<span data-ttu-id="e08d2-120">Nome da chave</span><span class="sxs-lookup"><span data-stu-id="e08d2-120">Name of the Key</span></span>

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

### <span data-ttu-id="e08d2-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e08d2-121">-Name</span></span>
<span data-ttu-id="e08d2-122">Nome do IotHub</span><span class="sxs-lookup"><span data-stu-id="e08d2-122">Name of the IotHub</span></span>

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

### <span data-ttu-id="e08d2-123">-RenewKey</span><span class="sxs-lookup"><span data-stu-id="e08d2-123">-RenewKey</span></span>
<span data-ttu-id="e08d2-124">Regenerar chave.</span><span class="sxs-lookup"><span data-stu-id="e08d2-124">Regenerate Key.</span></span>

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

### <span data-ttu-id="e08d2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e08d2-125">-ResourceGroupName</span></span>
<span data-ttu-id="e08d2-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e08d2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="e08d2-127">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e08d2-127">-Confirm</span></span>
<span data-ttu-id="e08d2-128">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e08d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08d2-129">-WhatIf</span></span>
<span data-ttu-id="e08d2-130">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e08d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e08d2-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e08d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08d2-132">CommonParameters</span></span>
<span data-ttu-id="e08d2-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e08d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08d2-134">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e08d2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08d2-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e08d2-135">INPUTS</span></span>

### <span data-ttu-id="e08d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e08d2-136">System.String</span></span>

## <span data-ttu-id="e08d2-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e08d2-137">OUTPUTS</span></span>

### <span data-ttu-id="e08d2-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSSharedAccessSignatureAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e08d2-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSSharedAccessSignatureAuthorizationRule</span></span>

## <span data-ttu-id="e08d2-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e08d2-139">NOTES</span></span>

## <span data-ttu-id="e08d2-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e08d2-140">RELATED LINKS</span></span>
