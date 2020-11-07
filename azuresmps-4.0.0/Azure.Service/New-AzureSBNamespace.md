---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945988"
---
# <span data-ttu-id="bef54-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="bef54-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="bef54-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bef54-102">SYNOPSIS</span></span>
<span data-ttu-id="bef54-103">Cria um namespace.</span><span class="sxs-lookup"><span data-stu-id="bef54-103">Creates a namespace.</span></span>

## <span data-ttu-id="bef54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bef54-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bef54-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bef54-105">DESCRIPTION</span></span>
<span data-ttu-id="bef54-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bef54-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="bef54-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="bef54-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="bef54-108">O cmdlet **New-AzureSBNamespace** cria um namespace de serviço para uso com o barramento de serviço no Azure.</span><span class="sxs-lookup"><span data-stu-id="bef54-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="bef54-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bef54-109">EXAMPLES</span></span>

### <span data-ttu-id="bef54-110">Exemplo 1: criar um namespace de serviço</span><span class="sxs-lookup"><span data-stu-id="bef54-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="bef54-111">Os exemplos criam um namespace de serviço para uso com o barramento de serviço no Azure.</span><span class="sxs-lookup"><span data-stu-id="bef54-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="bef54-112">Ambos os exemplos incluem os valores de parâmetro obrigatórios, mas somente o primeiro inclui os nomes dos parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bef54-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="bef54-113">O segundo exemplo pode ser usado porque ambos os parâmetros são posicionais e seus valores são fornecidos na ordem necessária.</span><span class="sxs-lookup"><span data-stu-id="bef54-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="bef54-114">OS</span><span class="sxs-lookup"><span data-stu-id="bef54-114">PARAMETERS</span></span>

### <span data-ttu-id="bef54-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="bef54-115">-CreateACSNamespace</span></span>
<span data-ttu-id="bef54-116">Especifica se você deve criar um namespace ACS associado além do namespace do serviço.</span><span class="sxs-lookup"><span data-stu-id="bef54-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef54-117">-Local</span><span class="sxs-lookup"><span data-stu-id="bef54-117">-Location</span></span>
<span data-ttu-id="bef54-118">Especifica uma região para o novo namespace.</span><span class="sxs-lookup"><span data-stu-id="bef54-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="bef54-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="bef54-119">-Name</span></span>
<span data-ttu-id="bef54-120">Especifica um nome para o novo namespace.</span><span class="sxs-lookup"><span data-stu-id="bef54-120">Specifies a name for the new namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef54-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="bef54-121">-NamespaceType</span></span>
<span data-ttu-id="bef54-122">Especifique se deseja usar o namespace para mensagens ou hubs de notificação.</span><span class="sxs-lookup"><span data-stu-id="bef54-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bef54-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="bef54-123">-Profile</span></span>
<span data-ttu-id="bef54-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="bef54-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="bef54-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="bef54-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bef54-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef54-126">CommonParameters</span></span>
<span data-ttu-id="bef54-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bef54-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef54-128">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bef54-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef54-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bef54-129">INPUTS</span></span>

## <span data-ttu-id="bef54-130">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bef54-130">OUTPUTS</span></span>

## <span data-ttu-id="bef54-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bef54-131">NOTES</span></span>

## <span data-ttu-id="bef54-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bef54-132">RELATED LINKS</span></span>

[<span data-ttu-id="bef54-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="bef54-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


