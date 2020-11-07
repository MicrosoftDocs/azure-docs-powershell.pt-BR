---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 163D2F00-E041-43A9-B077-9034F54B4F3D
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf258a8f13a344b09f9d5c7119cd78ad202d2ca0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945683"
---
# <span data-ttu-id="f5287-101">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="f5287-101">Enable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="f5287-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5287-102">SYNOPSIS</span></span>
<span data-ttu-id="f5287-103">Habilita o acesso à área de trabalho remota a um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="f5287-103">Enables remote desktop access to a cloud service.</span></span>

## <span data-ttu-id="f5287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5287-104">SYNTAX</span></span>

```
Enable-AzureServiceProjectRemoteDesktop -Username <String> -Password <SecureString> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f5287-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5287-105">DESCRIPTION</span></span>
<span data-ttu-id="f5287-106">Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f5287-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f5287-107">Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f5287-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f5287-108">O cmdlet **Enable-AzureServiceProjectRemoteDesktop** habilita o acesso à área de trabalho remota a um serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="f5287-108">The **Enable-AzureServiceProjectRemoteDesktop** cmdlet enables Remote Desktop access to a cloud service.</span></span>
<span data-ttu-id="f5287-109">Você deve publicar o serviço usando o cmdlet **Publish-AzureServiceProject** após habilitar o acesso à área de trabalho remota para que a alteração entre em vigor.</span><span class="sxs-lookup"><span data-stu-id="f5287-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after enabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="f5287-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5287-110">EXAMPLES</span></span>

## <span data-ttu-id="f5287-111">OS</span><span class="sxs-lookup"><span data-stu-id="f5287-111">PARAMETERS</span></span>

### <span data-ttu-id="f5287-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5287-112">-PassThru</span></span>
<span data-ttu-id="f5287-113">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f5287-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5287-114">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f5287-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5287-115">-Senha</span><span class="sxs-lookup"><span data-stu-id="f5287-115">-Password</span></span>
<span data-ttu-id="f5287-116">Especifica a senha.</span><span class="sxs-lookup"><span data-stu-id="f5287-116">Specifies the password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: pwd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5287-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f5287-117">-Profile</span></span>
<span data-ttu-id="f5287-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f5287-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5287-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f5287-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5287-120">-Username</span><span class="sxs-lookup"><span data-stu-id="f5287-120">-Username</span></span>
<span data-ttu-id="f5287-121">Especifica o nome de usuário a ser usado ao se conectar à instância de função no Azure por meio do protocolo de área de trabalho remota (RDP).</span><span class="sxs-lookup"><span data-stu-id="f5287-121">Specifies the user name to use when connecting to the role instance in Azure via the Remote Desktop Protocol (RDP).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: user

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5287-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5287-122">CommonParameters</span></span>
<span data-ttu-id="f5287-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5287-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5287-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5287-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5287-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5287-125">INPUTS</span></span>

## <span data-ttu-id="f5287-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5287-126">OUTPUTS</span></span>

## <span data-ttu-id="f5287-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5287-127">NOTES</span></span>

## <span data-ttu-id="f5287-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5287-128">RELATED LINKS</span></span>

[<span data-ttu-id="f5287-129">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="f5287-129">Disable-AzureServiceProjectRemoteDesktop</span></span>](./Disable-AzureServiceProjectRemoteDesktop.md)

[<span data-ttu-id="f5287-130">Publicar-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="f5287-130">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


