---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 6AB6C366-4925-4370-A33E-EDAF4BE1E230
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/remove-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Remove-AzMediaService.md
ms.openlocfilehash: 525c5e2bfd15811e861945a6404e0b88274e2563
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117558"
---
# <span data-ttu-id="1e750-101">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e750-101">Remove-AzMediaService</span></span>

## <span data-ttu-id="1e750-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1e750-102">SYNOPSIS</span></span>
<span data-ttu-id="1e750-103">Remove um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1e750-103">Removes a media service.</span></span>

## <span data-ttu-id="1e750-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e750-104">SYNTAX</span></span>

```
Remove-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e750-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e750-105">DESCRIPTION</span></span>
<span data-ttu-id="1e750-106">O cmdlet **Remove-AzMediaService** remove um serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1e750-106">The **Remove-AzMediaService** cmdlet removes a media service.</span></span>

## <span data-ttu-id="1e750-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e750-107">EXAMPLES</span></span>

### <span data-ttu-id="1e750-108">Exemplo 1: Remover um serviço de mídia</span><span class="sxs-lookup"><span data-stu-id="1e750-108">Example 1: Remove a media service</span></span>
```
PS C:\>Remove-AzMediaService -ResourceGroupName "ResourceGroup001" -AccountName "MediaService0011"
```

<span data-ttu-id="1e750-109">Esse comando remove o serviço de mídia chamado MediaService0011 no grupo de recursos chamado ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="1e750-109">This command removes the media service named MediaService0011 in the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="1e750-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e750-110">PARAMETERS</span></span>

### <span data-ttu-id="1e750-111">-NomedaEm conta</span><span class="sxs-lookup"><span data-stu-id="1e750-111">-AccountName</span></span>
<span data-ttu-id="1e750-112">Especifica o nome do serviço de mídia que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="1e750-112">Specifies the name of the media service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e750-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e750-113">-DefaultProfile</span></span>
<span data-ttu-id="1e750-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="1e750-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e750-115">-Forçar</span><span class="sxs-lookup"><span data-stu-id="1e750-115">-Force</span></span>
<span data-ttu-id="1e750-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e750-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1e750-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e750-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e750-118">Especifica o nome do grupo de recursos que contém o serviço de mídia.</span><span class="sxs-lookup"><span data-stu-id="1e750-118">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="1e750-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="1e750-119">-Confirm</span></span>
<span data-ttu-id="1e750-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e750-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e750-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e750-121">-WhatIf</span></span>
<span data-ttu-id="1e750-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="1e750-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e750-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1e750-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e750-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e750-124">CommonParameters</span></span>
<span data-ttu-id="1e750-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e750-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e750-126">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e750-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e750-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="1e750-127">INPUTS</span></span>

### <span data-ttu-id="1e750-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1e750-128">System.String</span></span>

## <span data-ttu-id="1e750-129">Saídas</span><span class="sxs-lookup"><span data-stu-id="1e750-129">OUTPUTS</span></span>

### <span data-ttu-id="1e750-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e750-130">System.Boolean</span></span>

## <span data-ttu-id="1e750-131">Notas</span><span class="sxs-lookup"><span data-stu-id="1e750-131">NOTES</span></span>

## <span data-ttu-id="1e750-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1e750-132">RELATED LINKS</span></span>

[<span data-ttu-id="1e750-133">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e750-133">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="1e750-134">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e750-134">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="1e750-135">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="1e750-135">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


