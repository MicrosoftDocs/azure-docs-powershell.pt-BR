---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: B96A64DD-9005-4B04-A720-6FCF33797E8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e1fa73aa4e38c8d222da6e73508e9a18a15c1e3f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946091"
---
# <span data-ttu-id="da6d6-101">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da6d6-101">Remove-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="da6d6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="da6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="da6d6-103">Remove um perfil do Gerenciador de tráfego.</span><span class="sxs-lookup"><span data-stu-id="da6d6-103">Removes a Traffic Manager profile.</span></span>

## <span data-ttu-id="da6d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="da6d6-104">SYNTAX</span></span>

```
Remove-AzureTrafficManagerProfile -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="da6d6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="da6d6-105">DESCRIPTION</span></span>
<span data-ttu-id="da6d6-106">O cmdlet **Remove-AzureTrafficManagerProfile** remove um perfil do Gerenciador de tráfego do Microsoft Azure da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="da6d6-106">The **Remove-AzureTrafficManagerProfile** cmdlet removes a Microsoft Azure Traffic Manager profile from the current subscription.</span></span>

## <span data-ttu-id="da6d6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="da6d6-107">EXAMPLES</span></span>

### <span data-ttu-id="da6d6-108">Exemplo 1: remover um perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="da6d6-108">Example 1: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="da6d6-109">Esse comando Remove o perfil do Gerenciador de tráfego chamado MyProfile.</span><span class="sxs-lookup"><span data-stu-id="da6d6-109">This command removes the Traffic Manager profile named MyProfile.</span></span>

### <span data-ttu-id="da6d6-110">Exemplo 2: remover um perfil do Gerenciador de tráfego</span><span class="sxs-lookup"><span data-stu-id="da6d6-110">Example 2: Remove a Traffic Manager profile</span></span>
```
PS C:\>Remove-AzureTrafficManagerProfile -Name "MyProfile" -Force -PassThru
```

<span data-ttu-id="da6d6-111">Esse comando Remove o perfil do Gerenciador de tráfego chamado MyProfile sem solicitar confirmação e retorna os resultados.</span><span class="sxs-lookup"><span data-stu-id="da6d6-111">This command removes the Traffic Manager profile named MyProfile without prompting you for confirmation, and returns the results.</span></span>

## <span data-ttu-id="da6d6-112">OS</span><span class="sxs-lookup"><span data-stu-id="da6d6-112">PARAMETERS</span></span>

### <span data-ttu-id="da6d6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="da6d6-113">-Force</span></span>
<span data-ttu-id="da6d6-114">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="da6d6-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da6d6-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="da6d6-115">-Name</span></span>
<span data-ttu-id="da6d6-116">Especifica o nome do perfil do Gerenciador de tráfego a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="da6d6-116">Specifies the name of the Traffic Manager profile to delete.</span></span>

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

### <span data-ttu-id="da6d6-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da6d6-117">-PassThru</span></span>
<span data-ttu-id="da6d6-118">Retorna $True se a operação for bem-sucedida; caso contrário, $False.</span><span class="sxs-lookup"><span data-stu-id="da6d6-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="da6d6-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="da6d6-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da6d6-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="da6d6-120">-Profile</span></span>
<span data-ttu-id="da6d6-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="da6d6-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="da6d6-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="da6d6-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da6d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da6d6-123">CommonParameters</span></span>
<span data-ttu-id="da6d6-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da6d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da6d6-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da6d6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da6d6-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="da6d6-126">INPUTS</span></span>

## <span data-ttu-id="da6d6-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="da6d6-127">OUTPUTS</span></span>

### <span data-ttu-id="da6d6-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="da6d6-128">System.Boolean</span></span>
<span data-ttu-id="da6d6-129">Este cmdlet gera $True ou $False.</span><span class="sxs-lookup"><span data-stu-id="da6d6-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="da6d6-130">Se a operação for bem-sucedida e se você especificar o parâmetro *PassThru* , esse cmdlet retornará um valor de $true.</span><span class="sxs-lookup"><span data-stu-id="da6d6-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="da6d6-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="da6d6-131">NOTES</span></span>

## <span data-ttu-id="da6d6-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="da6d6-132">RELATED LINKS</span></span>

[<span data-ttu-id="da6d6-133">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da6d6-133">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da6d6-134">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da6d6-134">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da6d6-135">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da6d6-135">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da6d6-136">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da6d6-136">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da6d6-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da6d6-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


