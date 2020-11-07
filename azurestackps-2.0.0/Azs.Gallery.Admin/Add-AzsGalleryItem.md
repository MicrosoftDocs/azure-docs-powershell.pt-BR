---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/add-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: d9ba42966efd4445fa561dff78b69d7e789badb5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93777138"
---
# <span data-ttu-id="2ea61-101">Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2ea61-101">Add-AzsGalleryItem</span></span>

## <span data-ttu-id="2ea61-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2ea61-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea61-103">Carrega um item de galeria de provedores para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ea61-103">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="2ea61-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2ea61-104">SYNTAX</span></span>

### <span data-ttu-id="2ea61-105">Createexpanded (padrão)</span><span class="sxs-lookup"><span data-stu-id="2ea61-105">CreateExpanded (Default)</span></span>
```
Add-AzsGalleryItem [-SubscriptionId <String>] [-GalleryItemUri <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2ea61-106">Criados</span><span class="sxs-lookup"><span data-stu-id="2ea61-106">Create</span></span>
```
Add-AzsGalleryItem -GalleryItemUriPayload <IGalleryItemUriPayload> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ea61-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2ea61-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea61-108">Carrega um item de galeria de provedores para o armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ea61-108">Uploads a provider gallery item to the storage.</span></span>

## <span data-ttu-id="2ea61-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2ea61-109">EXAMPLES</span></span>

### <span data-ttu-id="2ea61-110">Exemplo 1: Add-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2ea61-110">Example 1: Add-AzsGalleryItem</span></span>
```powershell
PS C:\> Add-AzsGalleryItem -GalleryItemUri https://testsa.blob.redmond.ext-n35r1010.masd.stbtest.microsoft.com/testsc/TestUbuntu.Test.1.0.0.azpkg

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM

```

<span data-ttu-id="2ea61-111">Carrega o TestUbuntu. Test. 1.0.0 para a galeria.</span><span class="sxs-lookup"><span data-stu-id="2ea61-111">Uploads TestUbuntu.Test.1.0.0 to the gallery.</span></span>

## <span data-ttu-id="2ea61-112">OS</span><span class="sxs-lookup"><span data-stu-id="2ea61-112">PARAMETERS</span></span>

### <span data-ttu-id="2ea61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea61-113">-DefaultProfile</span></span>
<span data-ttu-id="2ea61-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea61-115">-GalleryItemUri</span><span class="sxs-lookup"><span data-stu-id="2ea61-115">-GalleryItemUri</span></span>
<span data-ttu-id="2ea61-116">URI para o pacote da galeria que já foi carregado online.</span><span class="sxs-lookup"><span data-stu-id="2ea61-116">URI for your gallery package that has already been uploaded online.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea61-117">-GalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="2ea61-117">-GalleryItemUriPayload</span></span>
<span data-ttu-id="2ea61-118">Localização da carga do item da galeria.</span><span class="sxs-lookup"><span data-stu-id="2ea61-118">Location of gallery item payload.</span></span>
<span data-ttu-id="2ea61-119">Para construir, consulte a seção notas para propriedades GALLERYITEMURIPAYLOAD e crie uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="2ea61-119">To construct, see NOTES section for GALLERYITEMURIPAYLOAD properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2ea61-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ea61-120">-SubscriptionId</span></span>
<span data-ttu-id="2ea61-121">Credenciais de assinatura que identificam exclusivamente a assinatura do Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea61-121">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2ea61-122">A ID da assinatura forma a parte do URI para cada chamada de serviço.</span><span class="sxs-lookup"><span data-stu-id="2ea61-122">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea61-123">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2ea61-123">-Confirm</span></span>
<span data-ttu-id="2ea61-124">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ea61-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea61-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ea61-125">-WhatIf</span></span>
<span data-ttu-id="2ea61-126">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2ea61-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ea61-127">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2ea61-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2ea61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea61-128">CommonParameters</span></span>
<span data-ttu-id="2ea61-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea61-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ea61-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea61-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2ea61-131">INPUTS</span></span>

### <span data-ttu-id="2ea61-132">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. Api20150401. IGalleryItemUriPayload</span><span class="sxs-lookup"><span data-stu-id="2ea61-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItemUriPayload</span></span>

## <span data-ttu-id="2ea61-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2ea61-133">OUTPUTS</span></span>

### <span data-ttu-id="2ea61-134">Microsoft. Azure. PowerShell. cmdlets. Gallery. Models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="2ea61-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="2ea61-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2ea61-135">NOTES</span></span>

<span data-ttu-id="2ea61-136">Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas.</span><span class="sxs-lookup"><span data-stu-id="2ea61-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2ea61-137">Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2ea61-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2ea61-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload> : localização da carga do item da galeria.</span><span class="sxs-lookup"><span data-stu-id="2ea61-138">GALLERYITEMURIPAYLOAD <IGalleryItemUriPayload>: Location of gallery item payload.</span></span>
  - <span data-ttu-id="2ea61-139">`[GalleryItemUri <String>]`: URI para o pacote da galeria que já foi carregado online.</span><span class="sxs-lookup"><span data-stu-id="2ea61-139">`[GalleryItemUri <String>]`: URI for your gallery package that has already been uploaded online.</span></span>

## <span data-ttu-id="2ea61-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2ea61-140">RELATED LINKS</span></span>

