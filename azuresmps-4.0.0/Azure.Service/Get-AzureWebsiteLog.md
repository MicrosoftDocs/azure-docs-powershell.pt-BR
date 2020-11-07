---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: BFB57100-93F6-4FD2-8ECA-7F54BEB0D6B0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7114f39ee2b105c80429151df8347b5c17dcfea0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946506"
---
# <span data-ttu-id="8295f-101">Get-AzureWebsiteLog</span><span class="sxs-lookup"><span data-stu-id="8295f-101">Get-AzureWebsiteLog</span></span>

## <span data-ttu-id="8295f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8295f-102">SYNOPSIS</span></span>
<span data-ttu-id="8295f-103">Obtém logs para o site especificado.</span><span class="sxs-lookup"><span data-stu-id="8295f-103">Gets logs for the specified website.</span></span>

## <span data-ttu-id="8295f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8295f-104">SYNTAX</span></span>

### <span data-ttu-id="8295f-105">Eletrônico</span><span class="sxs-lookup"><span data-stu-id="8295f-105">Tail</span></span>
```
Get-AzureWebsiteLog [-Path <String>] [-Message <String>] [-Tail] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8295f-106">ListPath</span><span class="sxs-lookup"><span data-stu-id="8295f-106">ListPath</span></span>
```
Get-AzureWebsiteLog [-ListPath] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="8295f-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8295f-107">DESCRIPTION</span></span>
<span data-ttu-id="8295f-108">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8295f-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8295f-109">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8295f-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8295f-110">Obtém log para o site especificado.</span><span class="sxs-lookup"><span data-stu-id="8295f-110">Gets log for the specified website.</span></span>

## <span data-ttu-id="8295f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8295f-111">EXAMPLES</span></span>

### <span data-ttu-id="8295f-112">Exemplo 1: iniciar o fluxo de log</span><span class="sxs-lookup"><span data-stu-id="8295f-112">Example 1: Start log streaming</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail
```

<span data-ttu-id="8295f-113">Este exemplo inicia o streaming de log para todos os logs de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8295f-113">This example starts log streaming for all application logs.</span></span>

### <span data-ttu-id="8295f-114">Exemplo 2: iniciar o fluxo de log para logs http</span><span class="sxs-lookup"><span data-stu-id="8295f-114">Example 2: Start log streaming for http logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Path http
```

<span data-ttu-id="8295f-115">Este exemplo inicia o fluxo de log para logs http.</span><span class="sxs-lookup"><span data-stu-id="8295f-115">This example starts log streaming for http logs.</span></span>

### <span data-ttu-id="8295f-116">Exemplo 3: iniciar o fluxo de log para logs de erros</span><span class="sxs-lookup"><span data-stu-id="8295f-116">Example 3: Start log streaming for error logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Tail -Message Error
```

<span data-ttu-id="8295f-117">Este exemplo inicia o fluxo de log e mostra apenas logs de erros.</span><span class="sxs-lookup"><span data-stu-id="8295f-117">This example starts log streaming and show error logs only.</span></span>

### <span data-ttu-id="8295f-118">Exemplo 4: Exibir logs indisponívels</span><span class="sxs-lookup"><span data-stu-id="8295f-118">Example 4: Display avaiable logs</span></span>
```
PS C:\> Get-AzureWebsiteLog -Name MyWebsite -ListPath
```

<span data-ttu-id="8295f-119">Este exemplo lista todos os caminhos de log disponíveis no website.</span><span class="sxs-lookup"><span data-stu-id="8295f-119">This example lists all available log paths in the website.</span></span>

## <span data-ttu-id="8295f-120">OS</span><span class="sxs-lookup"><span data-stu-id="8295f-120">PARAMETERS</span></span>

### <span data-ttu-id="8295f-121">-ListPath</span><span class="sxs-lookup"><span data-stu-id="8295f-121">-ListPath</span></span>
<span data-ttu-id="8295f-122">Indica se os caminhos de log devem ser listados.</span><span class="sxs-lookup"><span data-stu-id="8295f-122">Indicates whether to list the log paths.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListPath
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295f-123">-Mensagem</span><span class="sxs-lookup"><span data-stu-id="8295f-123">-Message</span></span>
<span data-ttu-id="8295f-124">Especifica uma cadeia de caracteres que será usada para filtrar a mensagem de log.</span><span class="sxs-lookup"><span data-stu-id="8295f-124">Specifies a string which will be used to filter the log message.</span></span>
<span data-ttu-id="8295f-125">Somente os logs que contêm essa cadeia de caracteres serão recuperados.</span><span class="sxs-lookup"><span data-stu-id="8295f-125">Only logs which contains this string will be retrieved.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295f-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8295f-126">-Name</span></span>
<span data-ttu-id="8295f-127">O nome do site.</span><span class="sxs-lookup"><span data-stu-id="8295f-127">The name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295f-128">-Caminho</span><span class="sxs-lookup"><span data-stu-id="8295f-128">-Path</span></span>
<span data-ttu-id="8295f-129">O caminho a partir do qual o log será recuperado.</span><span class="sxs-lookup"><span data-stu-id="8295f-129">The path from which the log will be retrieved.</span></span>
<span data-ttu-id="8295f-130">Por padrão, é raiz, o que significa incluir todos os caminhos.</span><span class="sxs-lookup"><span data-stu-id="8295f-130">By default it is Root, which means include all the paths.</span></span>

```yaml
Type: String
Parameter Sets: Tail
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295f-131">-Perfil</span><span class="sxs-lookup"><span data-stu-id="8295f-131">-Profile</span></span>
<span data-ttu-id="8295f-132">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="8295f-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8295f-133">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="8295f-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8295f-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="8295f-134">-Slot</span></span>
<span data-ttu-id="8295f-135">Especifica o nome do slot.</span><span class="sxs-lookup"><span data-stu-id="8295f-135">Specifies the slot name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295f-136">-Caudal</span><span class="sxs-lookup"><span data-stu-id="8295f-136">-Tail</span></span>
<span data-ttu-id="8295f-137">Especifica se os logs devem ser transmitidos.</span><span class="sxs-lookup"><span data-stu-id="8295f-137">Specifies whether to stream the logs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Tail
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8295f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8295f-138">CommonParameters</span></span>
<span data-ttu-id="8295f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8295f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8295f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8295f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8295f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8295f-141">INPUTS</span></span>

## <span data-ttu-id="8295f-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8295f-142">OUTPUTS</span></span>

## <span data-ttu-id="8295f-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8295f-143">NOTES</span></span>

## <span data-ttu-id="8295f-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8295f-144">RELATED LINKS</span></span>

[<span data-ttu-id="8295f-145">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8295f-145">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="8295f-146">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8295f-146">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="8295f-147">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8295f-147">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)

[<span data-ttu-id="8295f-148">Start-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="8295f-148">Start-AzureWebsite</span></span>](./Start-AzureWebsite.md)


