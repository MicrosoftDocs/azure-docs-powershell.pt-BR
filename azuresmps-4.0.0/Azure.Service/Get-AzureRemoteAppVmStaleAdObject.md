---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945630"
---
# <span data-ttu-id="ed29d-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="ed29d-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="ed29d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed29d-102">SYNOPSIS</span></span>
<span data-ttu-id="ed29d-103">Obtém objetos no Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.</span><span class="sxs-lookup"><span data-stu-id="ed29d-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="ed29d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed29d-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ed29d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed29d-105">DESCRIPTION</span></span>
<span data-ttu-id="ed29d-106">O cmdlet **Get-AzureRemoteAppVmStaleAdObject** obtém objetos do Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.</span><span class="sxs-lookup"><span data-stu-id="ed29d-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="ed29d-107">Esse cmdlet exibe o nome de cada objeto que ele obtém.</span><span class="sxs-lookup"><span data-stu-id="ed29d-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="ed29d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed29d-108">EXAMPLES</span></span>

### <span data-ttu-id="ed29d-109">Exemplo 1: obter objetos obsoletos para uma coleção</span><span class="sxs-lookup"><span data-stu-id="ed29d-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="ed29d-110">Este segundo comando obtém os objetos obsoletos da coleção chamada contoso.</span><span class="sxs-lookup"><span data-stu-id="ed29d-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="ed29d-111">OS</span><span class="sxs-lookup"><span data-stu-id="ed29d-111">PARAMETERS</span></span>

### <span data-ttu-id="ed29d-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="ed29d-112">-CollectionName</span></span>
<span data-ttu-id="ed29d-113">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ed29d-113">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="ed29d-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="ed29d-114">-Credential</span></span>
<span data-ttu-id="ed29d-115">Especifica uma credencial que tem direitos para executar esta ação.</span><span class="sxs-lookup"><span data-stu-id="ed29d-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="ed29d-116">Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="ed29d-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="ed29d-117">Se você não especificar esse parâmetro, esse cmdlet usará as credenciais do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="ed29d-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

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

### <span data-ttu-id="ed29d-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ed29d-118">-Profile</span></span>
<span data-ttu-id="ed29d-119">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ed29d-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ed29d-120">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ed29d-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ed29d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed29d-121">CommonParameters</span></span>
<span data-ttu-id="ed29d-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed29d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed29d-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed29d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed29d-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed29d-124">INPUTS</span></span>

## <span data-ttu-id="ed29d-125">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed29d-125">OUTPUTS</span></span>

### <span data-ttu-id="ed29d-126">String</span><span class="sxs-lookup"><span data-stu-id="ed29d-126">String</span></span>

## <span data-ttu-id="ed29d-127">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed29d-127">NOTES</span></span>

## <span data-ttu-id="ed29d-128">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed29d-128">RELATED LINKS</span></span>

[<span data-ttu-id="ed29d-129">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="ed29d-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


