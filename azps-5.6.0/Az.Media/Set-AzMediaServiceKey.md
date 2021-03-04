---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: D28EB28D-DBC6-48D5-AB0A-C56F56CD0104
online version: https://docs.microsoft.com/powershell/module/az.media/set-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Set-AzMediaServiceKey.md
ms.openlocfilehash: 43e98ae0c6aa05123a291704baeb5855e8e3b1af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889259"
---
# <span data-ttu-id="2f321-101">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="2f321-101">Set-AzMediaServiceKey</span></span>

## <span data-ttu-id="2f321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f321-102">SYNOPSIS</span></span>
<span data-ttu-id="2f321-103">Regenera uma chave usada para acessar o ponto de extremidade REST associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2f321-103">Regenerates a key used for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="2f321-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2f321-104">SYNTAX</span></span>

```
Set-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String> [-KeyType] <KeyType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f321-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2f321-105">DESCRIPTION</span></span>
<span data-ttu-id="2f321-106">O cmdlet **Set-AzMediaServiceKey** regenera uma chave usada para acessar o ponto de extremidade REST (Transferência de Estado Representacional) associado ao serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2f321-106">The **Set-AzMediaServiceKey** cmdlet regenerates a key used for accessing the Representational State Transfer (REST) endpoint associated with the media service.</span></span>

## <span data-ttu-id="2f321-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2f321-107">EXAMPLES</span></span>

### <span data-ttu-id="2f321-108">Exemplo 1: Regenerar a chave primária usada para acessar o Serviço de Mídia</span><span class="sxs-lookup"><span data-stu-id="2f321-108">Example 1: Regenerate the primary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "ResourceGroup004" -AccountName "MediaService001" -KeyType Primary
```

<span data-ttu-id="2f321-109">Este comando regenera a chave primária do serviço de mídia chamado MediaService001 que pertence ao grupo de recursos chamado ResourceGroup004.</span><span class="sxs-lookup"><span data-stu-id="2f321-109">This command regenerates the primary key for the media service named MediaService001 that belongs to the resource group named ResourceGroup004.</span></span>

### <span data-ttu-id="2f321-110">Exemplo 2: regenera a chave secundária usada para acessar o Serviço de Mídia</span><span class="sxs-lookup"><span data-stu-id="2f321-110">Example 2: Regenerates the secondary key used for accessing the Media Service</span></span>
```
PS C:\>Set-AzMediaServiceKey -ResourceGroupName "Resourcegroup123" -AccountName "MediaService002" -KeyType Secondary
```

<span data-ttu-id="2f321-111">Esse comando regenera a chave secundária do serviço de mídia chamado MediaService002 que pertence ao grupo de recursos chamado Resourcegroup123.</span><span class="sxs-lookup"><span data-stu-id="2f321-111">This command regenerates the secondary key for the media service named MediaService002 that belongs to the resource group named Resourcegroup123.</span></span>

## <span data-ttu-id="2f321-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2f321-112">PARAMETERS</span></span>

### <span data-ttu-id="2f321-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2f321-113">-AccountName</span></span>
<span data-ttu-id="2f321-114">Especifica o nome do serviço de mídia que este cmdlet regenera.</span><span class="sxs-lookup"><span data-stu-id="2f321-114">Specifies the name of the media service that this cmdlet regenerates.</span></span>

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

### <span data-ttu-id="2f321-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f321-115">-DefaultProfile</span></span>
<span data-ttu-id="2f321-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2f321-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f321-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="2f321-117">-KeyType</span></span>
<span data-ttu-id="2f321-118">Especifica o tipo de chave do serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2f321-118">Specifies the key type of the media service.</span></span>
<span data-ttu-id="2f321-119">Os valores aceitáveis para este parâmetro são: Primário ou Secundário.</span><span class="sxs-lookup"><span data-stu-id="2f321-119">The acceptable values for this parameter are: Primary or Secondary.</span></span>

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

### <span data-ttu-id="2f321-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f321-120">-ResourceGroupName</span></span>
<span data-ttu-id="2f321-121">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="2f321-121">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="2f321-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f321-122">-Confirm</span></span>
<span data-ttu-id="2f321-123">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f321-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f321-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f321-124">-WhatIf</span></span>
<span data-ttu-id="2f321-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2f321-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f321-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2f321-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f321-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f321-127">CommonParameters</span></span>
<span data-ttu-id="2f321-128">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f321-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f321-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f321-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f321-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f321-130">INPUTS</span></span>

### <span data-ttu-id="2f321-131">System.String</span><span class="sxs-lookup"><span data-stu-id="2f321-131">System.String</span></span>

## <span data-ttu-id="2f321-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2f321-132">OUTPUTS</span></span>

### <span data-ttu-id="2f321-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span><span class="sxs-lookup"><span data-stu-id="2f321-133">Microsoft.Azure.Commands.Media.Models.PSServiceKey</span></span>

## <span data-ttu-id="2f321-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="2f321-134">NOTES</span></span>

## <span data-ttu-id="2f321-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2f321-135">RELATED LINKS</span></span>

[<span data-ttu-id="2f321-136">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="2f321-136">Get-AzMediaServiceKey</span></span>](./Get-AzMediaServiceKey.md)


