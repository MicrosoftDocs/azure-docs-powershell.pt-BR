---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946375"
---
# <span data-ttu-id="0cd0a-101">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cd0a-101">Enable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="0cd0a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0cd0a-102">SYNOPSIS</span></span>
<span data-ttu-id="0cd0a-103">Habilita um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-103">Enables a Traffic Manager profile.</span></span>

## <span data-ttu-id="0cd0a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0cd0a-104">SYNTAX</span></span>

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0cd0a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0cd0a-105">DESCRIPTION</span></span>
<span data-ttu-id="0cd0a-106">O cmdlet **Enable-AzureTrafficManagerProfile** habilita um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-106">The **Enable-AzureTrafficManagerProfile** cmdlet enables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0cd0a-107">Especifique o parâmetro *PassThru* para exibir se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-107">Specify the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="0cd0a-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0cd0a-108">EXAMPLES</span></span>

### <span data-ttu-id="0cd0a-109">Exemplo 1: habilitar um perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="0cd0a-109">Example 1: Enable a Traffic Manager profile</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="0cd0a-110">Esse comando habilita o perfil do Gerenciador de tráfego chamado MyProfile.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-110">This command enables the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="0cd0a-111">Exemplo 2: habilitar um perfil do Gerenciador de tráfego e exibir os resultados</span><span class="sxs-lookup"><span data-stu-id="0cd0a-111">Example 2: Enable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="0cd0a-112">Esse comando habilita o perfil do Gerenciador de tráfego chamado MyProfile e exibe se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-112">This command enables the Traffic Manager profile named MyProfile and displays whether the command succeeded.</span></span>

## <span data-ttu-id="0cd0a-113">OS</span><span class="sxs-lookup"><span data-stu-id="0cd0a-113">PARAMETERS</span></span>

### <span data-ttu-id="0cd0a-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0cd0a-114">-Name</span></span>
<span data-ttu-id="0cd0a-115">Especifica o nome do perfil do Gerenciador de tráfego a ser habilitado.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-115">Specifies the name of the Traffic Manager profile to enable.</span></span>

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

### <span data-ttu-id="0cd0a-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cd0a-116">-PassThru</span></span>
<span data-ttu-id="0cd0a-117">Retorna $True se a operação for bem-sucedida; caso contrário, $False.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-117">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="0cd0a-118">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-118">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cd0a-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0cd0a-119">-Profile</span></span>
<span data-ttu-id="0cd0a-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-120">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0cd0a-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0cd0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cd0a-122">CommonParameters</span></span>
<span data-ttu-id="0cd0a-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cd0a-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cd0a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cd0a-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0cd0a-125">INPUTS</span></span>

## <span data-ttu-id="0cd0a-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0cd0a-126">OUTPUTS</span></span>

### <span data-ttu-id="0cd0a-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0cd0a-127">System.Boolean</span></span>
<span data-ttu-id="0cd0a-128">Este cmdlet gera $True ou $False.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-128">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="0cd0a-129">Se a operação for bem-sucedida e se você especificar o parâmetro *PassThru* , esse cmdlet retornará um valor de $true.</span><span class="sxs-lookup"><span data-stu-id="0cd0a-129">If the operation succeeds and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="0cd0a-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0cd0a-130">NOTES</span></span>

## <span data-ttu-id="0cd0a-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0cd0a-131">RELATED LINKS</span></span>

[<span data-ttu-id="0cd0a-132">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cd0a-132">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0cd0a-133">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cd0a-133">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0cd0a-134">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cd0a-134">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0cd0a-135">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cd0a-135">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0cd0a-136">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0cd0a-136">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


