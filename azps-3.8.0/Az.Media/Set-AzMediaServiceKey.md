---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 0a7dc826aae7efebfc3d24bdeba02c75d0bf5a03
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944524"
---
# <span data-ttu-id="cbc06-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="cbc06-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="cbc06-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbc06-102">SYNOPSIS</span></span>
<span data-ttu-id="cbc06-103">Gera novamente uma chave usada para acessar o ponto de extremidade restante associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cbc06-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="cbc06-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbc06-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbc06-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbc06-105">DESCRIPTION</span></span>
<span data-ttu-id="cbc06-106">O cmdlet **set-AzMediaServiceKey** regenera uma chave usada para acessar o ponto de extremidade do REST (transferência de estado representational) associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cbc06-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="cbc06-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbc06-107">EXAMPLES</span></span>

### <span data-ttu-id="cbc06-108">Exemplo 1: regenerar a chave primária usada para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="cbc06-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="cbc06-109">Esse comando regenera a chave primária para o serviço de mídia denominado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="cbc06-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="cbc06-110">Exemplo 2: regenera a chave secundária usada para acessar o serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="cbc06-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="cbc06-111">Esse comando regenera a chave secundária para o serviço de mídia denominado MediaService002 que pertence ao grupo de recursos chamado Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="cbc06-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="cbc06-112">OS</span><span class="sxs-lookup"><span data-stu-id="cbc06-112">PARAMETERS</span></span>

### <span data-ttu-id="cbc06-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cbc06-113">-AccountName</span></span>
<span data-ttu-id="cbc06-114">Especifica o nome do serviço de mídia que este cmdlet gera novamente.</span><span class="sxs-lookup"><span data-stu-id="cbc06-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="cbc06-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbc06-115">-DefaultProfile</span></span>
<span data-ttu-id="cbc06-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cbc06-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbc06-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="cbc06-117">-KeyType</span></span>
<span data-ttu-id="cbc06-118">Especifica o tipo de chave do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cbc06-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="cbc06-119">Os valores aceitáveis para esse parâmetro são: Primary ou Secondary.</span><span class="sxs-lookup"><span data-stu-id="cbc06-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="cbc06-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbc06-120">-ResourceGroupName</span></span>
<span data-ttu-id="cbc06-121">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cbc06-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="cbc06-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbc06-122">-Confirm</span></span>
<span data-ttu-id="cbc06-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbc06-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbc06-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbc06-124">-WhatIf</span></span>
<span data-ttu-id="cbc06-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbc06-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbc06-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbc06-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbc06-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbc06-127">CommonParameters</span></span>
<span data-ttu-id="cbc06-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbc06-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbc06-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbc06-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbc06-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbc06-130">INPUTS</span></span>

### <span data-ttu-id="cbc06-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cbc06-131">System.String</span></span>

## <span data-ttu-id="cbc06-132">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbc06-132">OUTPUTS</span></span>

### <span data-ttu-id="cbc06-133">Microsoft. Azure. Commands. Media. Models. PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="cbc06-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="cbc06-134">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbc06-134">NOTES</span></span>

## <span data-ttu-id="cbc06-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbc06-135">RELATED LINKS</span></span>

[<span data-ttu-id="cbc06-136">Get-AzMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="cbc06-136">Get-AzMediaServiceKeys</span></span>](./Get-AzMediaServiceKeys.md)


