---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945693"
---
# <span data-ttu-id="b7acb-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7acb-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="b7acb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7acb-102">SYNOPSIS</span></span>
<span data-ttu-id="b7acb-103">Desabilita um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="b7acb-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="b7acb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7acb-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b7acb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7acb-105">DESCRIPTION</span></span>
<span data-ttu-id="b7acb-106">O cmdlet **Disable-AzureTrafficManagerProfile** desabilita um perfil do Gerenciador de tráfego do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7acb-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b7acb-107">Você pode usar o parâmetro *PassThru* para exibir se a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b7acb-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="b7acb-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7acb-108">EXAMPLES</span></span>

### <span data-ttu-id="b7acb-109">Exemplo 1: desabilitar um perfil do Gerenciador de tráfego e exibir os resultados</span><span class="sxs-lookup"><span data-stu-id="b7acb-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="b7acb-110">Esse comando desabilita o perfil do Gerenciador de tráfego chamado MyProfile.</span><span class="sxs-lookup"><span data-stu-id="b7acb-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="b7acb-111">O comando especifica o parâmetro *PassThru* para exibir se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b7acb-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="b7acb-112">Exemplo 2: desabilitar um perfil do Gerenciador de tráfego e exibir nenhum resultado</span><span class="sxs-lookup"><span data-stu-id="b7acb-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="b7acb-113">Esse comando desabilita o perfil do Gerenciador de tráfego chamado MyProfile, mas não exibe se o comando foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b7acb-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="b7acb-114">OS</span><span class="sxs-lookup"><span data-stu-id="b7acb-114">PARAMETERS</span></span>

### <span data-ttu-id="b7acb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7acb-115">-Name</span></span>
<span data-ttu-id="b7acb-116">Especifica o nome do perfil do Gerenciador de tráfego a ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="b7acb-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="b7acb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7acb-117">-PassThru</span></span>
<span data-ttu-id="b7acb-118">Retorna $True se a operação for bem-sucedida; caso contrário, $False.</span><span class="sxs-lookup"><span data-stu-id="b7acb-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="b7acb-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="b7acb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7acb-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="b7acb-120">-Profile</span></span>
<span data-ttu-id="b7acb-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="b7acb-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b7acb-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="b7acb-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7acb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7acb-123">CommonParameters</span></span>
<span data-ttu-id="b7acb-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7acb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7acb-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7acb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7acb-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7acb-126">INPUTS</span></span>

## <span data-ttu-id="b7acb-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7acb-127">OUTPUTS</span></span>

### <span data-ttu-id="b7acb-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7acb-128">System.Boolean</span></span>
<span data-ttu-id="b7acb-129">Este cmdlet gera $True ou $False.</span><span class="sxs-lookup"><span data-stu-id="b7acb-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="b7acb-130">Se a operação for bem-sucedida e se você especificar o parâmetro *PassThru* , esse cmdlet retornará um valor de $true.</span><span class="sxs-lookup"><span data-stu-id="b7acb-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="b7acb-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7acb-131">NOTES</span></span>

## <span data-ttu-id="b7acb-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7acb-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7acb-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7acb-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b7acb-134">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7acb-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b7acb-135">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7acb-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b7acb-136">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7acb-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b7acb-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b7acb-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


