---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/remove-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Remove-AzureRmMediaService.md
ms.openlocfilehash: 9ddf8291d5f6276126cea82305bbc554d05ca006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440374"
---
# <span data-ttu-id="cefb3-101">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cefb3-101">Remove-AzureRmMediaService</span></span>

## <span data-ttu-id="cefb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cefb3-102">SYNOPSIS</span></span>
<span data-ttu-id="cefb3-103">Remove um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cefb3-103">Removes a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cefb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cefb3-104">SYNTAX</span></span>

```
Remove-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cefb3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cefb3-105">DESCRIPTION</span></span>
<span data-ttu-id="cefb3-106">O cmdlet **Remove-AzureRmMediaService** remove um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cefb3-106">The **Remove-AzureRmMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="cefb3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cefb3-107">EXAMPLES</span></span>

### <span data-ttu-id="cefb3-108">Exemplo 1: remover um serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="cefb3-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzureRmMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="cefb3-109">Esse comando Remove o serviço de mídia chamado MediaService0011 no grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="cefb3-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="cefb3-110">OS</span><span class="sxs-lookup"><span data-stu-id="cefb3-110">PARAMETERS</span></span>

### <span data-ttu-id="cefb3-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cefb3-111">-AccountName</span></span>
<span data-ttu-id="cefb3-112">Especifica o nome do serviço de mídia que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="cefb3-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cefb3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefb3-113">-DefaultProfile</span></span>
<span data-ttu-id="cefb3-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="cefb3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cefb3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cefb3-115">-Force</span></span>
<span data-ttu-id="cefb3-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="cefb3-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cefb3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cefb3-117">-ResourceGroupName</span></span>
<span data-ttu-id="cefb3-118">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="cefb3-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="cefb3-119">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cefb3-119">-Confirm</span></span>
<span data-ttu-id="cefb3-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cefb3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cefb3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cefb3-121">-WhatIf</span></span>
<span data-ttu-id="cefb3-122">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cefb3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cefb3-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cefb3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cefb3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefb3-124">CommonParameters</span></span>
<span data-ttu-id="cefb3-125">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cefb3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefb3-126">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cefb3-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefb3-127">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cefb3-127">INPUTS</span></span>

### <span data-ttu-id="cefb3-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cefb3-128">System.String</span></span>

## <span data-ttu-id="cefb3-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cefb3-129">OUTPUTS</span></span>

### <span data-ttu-id="cefb3-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cefb3-130">System.Boolean</span></span>

## <span data-ttu-id="cefb3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cefb3-131">NOTES</span></span>

## <span data-ttu-id="cefb3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cefb3-132">RELATED LINKS</span></span>

[<span data-ttu-id="cefb3-133">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cefb3-133">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="cefb3-134">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cefb3-134">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="cefb3-135">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="cefb3-135">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


