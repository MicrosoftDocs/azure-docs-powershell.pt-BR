---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945703"
---
# <span data-ttu-id="f5a77-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="f5a77-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="f5a77-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5a77-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a77-103">Remove objetos no Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.</span><span class="sxs-lookup"><span data-stu-id="f5a77-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="f5a77-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5a77-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a77-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5a77-105">DESCRIPTION</span></span>
<span data-ttu-id="f5a77-106">O cmdlet **Clear-AzureRemoteAppVmStaleAdObject** remove objetos do Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.</span><span class="sxs-lookup"><span data-stu-id="f5a77-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="f5a77-107">Você deve usar credenciais que tenham direitos para remover objetos do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f5a77-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="f5a77-108">Se você especificar o parâmetro Common *Verbose* , esse cmdlet exibirá o nome de cada objeto que ele excluir.</span><span class="sxs-lookup"><span data-stu-id="f5a77-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="f5a77-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5a77-109">EXAMPLES</span></span>

### <span data-ttu-id="f5a77-110">Exemplo 1: limpar objetos obsoletos para uma coleção</span><span class="sxs-lookup"><span data-stu-id="f5a77-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="f5a77-111">O primeiro comando solicita um nome de usuário e uma senha usando **Get-Credential**.</span><span class="sxs-lookup"><span data-stu-id="f5a77-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="f5a77-112">O comando armazena os resultados na variável $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="f5a77-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="f5a77-113">O segundo comando limpa os objetos obsoletos da coleção chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="f5a77-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="f5a77-114">O comando usa as credenciais armazenadas na variável $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="f5a77-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="f5a77-115">Para que o comando tenha êxito, essas credenciais devem ter direitos apropriados.</span><span class="sxs-lookup"><span data-stu-id="f5a77-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="f5a77-116">OS</span><span class="sxs-lookup"><span data-stu-id="f5a77-116">PARAMETERS</span></span>

### <span data-ttu-id="f5a77-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="f5a77-117">-CollectionName</span></span>
<span data-ttu-id="f5a77-118">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="f5a77-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5a77-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="f5a77-119">-Credential</span></span>
<span data-ttu-id="f5a77-120">Especifica uma credencial que tem direitos para executar esta ação.</span><span class="sxs-lookup"><span data-stu-id="f5a77-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="f5a77-121">Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="f5a77-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="f5a77-122">Se você não especificar esse parâmetro, esse cmdlet usará as credenciais do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="f5a77-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a77-123">-Perfil</span><span class="sxs-lookup"><span data-stu-id="f5a77-123">-Profile</span></span>
<span data-ttu-id="f5a77-124">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="f5a77-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f5a77-125">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="f5a77-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f5a77-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5a77-126">-Confirm</span></span>
<span data-ttu-id="f5a77-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5a77-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a77-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a77-128">-WhatIf</span></span>
<span data-ttu-id="f5a77-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5a77-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a77-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5a77-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5a77-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a77-131">CommonParameters</span></span>
<span data-ttu-id="f5a77-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5a77-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a77-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a77-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a77-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5a77-134">INPUTS</span></span>

## <span data-ttu-id="f5a77-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5a77-135">OUTPUTS</span></span>

## <span data-ttu-id="f5a77-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5a77-136">NOTES</span></span>

## <span data-ttu-id="f5a77-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5a77-137">RELATED LINKS</span></span>

[<span data-ttu-id="f5a77-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="f5a77-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


