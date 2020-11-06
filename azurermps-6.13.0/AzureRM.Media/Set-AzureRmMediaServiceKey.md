---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/set-azurermmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Set-AzureRmMediaServiceKey.md
ms.openlocfilehash: 10de62fd77fa62f83373637e844edd436dd0681f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440770"
---
# <span data-ttu-id="6fda9-101">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="6fda9-101">Set-AzureRmMediaServiceKey</span></span>

## <span data-ttu-id="6fda9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fda9-102">SYNOPSIS</span></span>
<span data-ttu-id="6fda9-103">Gera novamente uma chave usada para acessar o ponto de extremidade restante associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="6fda9-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fda9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fda9-104">SYNTAX</span></span>

```
Set-AzureRmMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fda9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fda9-105">DESCRIPTION</span></span>
<span data-ttu-id="6fda9-106">O cmdlet **set-AzureRmMediaServiceKey** regenera uma chave usada para acessar o ponto de extremidade do REST (transferência de estado representational) associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="6fda9-106">The **Set-AzureRmMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="6fda9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fda9-107">EXAMPLES</span></span>

### <span data-ttu-id="6fda9-108">Exemplo 1: regenerar a chave primária usada para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="6fda9-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="6fda9-109">Esse comando regenera a chave primária para o serviço de mídia denominado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="6fda9-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="6fda9-110">Exemplo 2: regenera a chave secundária usada para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="6fda9-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzureRmMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="6fda9-111">Esse comando regenera a chave secundária para o serviço de mídia denominado MediaService002 que pertence ao grupo de recursos chamado Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="6fda9-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="6fda9-112">OS</span><span class="sxs-lookup"><span data-stu-id="6fda9-112">PARAMETERS</span></span>

### <span data-ttu-id="6fda9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6fda9-113">-AccountName</span></span>
<span data-ttu-id="6fda9-114">Especifica o nome do serviço de mídia que este cmdlet gera novamente.</span><span class="sxs-lookup"><span data-stu-id="6fda9-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fda9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fda9-115">-DefaultProfile</span></span>
<span data-ttu-id="6fda9-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6fda9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fda9-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="6fda9-117">-KeyType</span></span>
<span data-ttu-id="6fda9-118">Especifica o tipo de chave do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="6fda9-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="6fda9-119">Os valores aceitáveis para esse parâmetro são: Primary ou Secondary.</span><span class="sxs-lookup"><span data-stu-id="6fda9-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

```yaml
Type: Microsoft.Azure.Management.Media.Models.KeyType
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fda9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fda9-120">-ResourceGroupName</span></span>
<span data-ttu-id="6fda9-121">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="6fda9-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="6fda9-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6fda9-122">-Confirm</span></span>
<span data-ttu-id="6fda9-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fda9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fda9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fda9-124">-WhatIf</span></span>
<span data-ttu-id="6fda9-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6fda9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fda9-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6fda9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fda9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fda9-127">CommonParameters</span></span>
<span data-ttu-id="6fda9-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fda9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fda9-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fda9-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fda9-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fda9-130">INPUTS</span></span>

### <span data-ttu-id="6fda9-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6fda9-131">System.String</span></span>

## <span data-ttu-id="6fda9-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fda9-132">OUTPUTS</span></span>

### <span data-ttu-id="6fda9-133">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="6fda9-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="6fda9-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fda9-134">NOTES</span></span>

## <span data-ttu-id="6fda9-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fda9-135">RELATED LINKS</span></span>

[<span data-ttu-id="6fda9-136">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="6fda9-136">Get-AzureRmMediaServiceKeys</span></span>](./Get-AzureRmMediaServiceKeys.md)


