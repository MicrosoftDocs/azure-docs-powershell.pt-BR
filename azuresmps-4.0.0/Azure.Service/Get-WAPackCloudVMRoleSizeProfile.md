---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946508"
---
# <span data-ttu-id="34e96-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="34e96-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="34e96-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="34e96-102">SYNOPSIS</span></span>
<span data-ttu-id="34e96-103">Obtém objetos de perfil do tamanho da função MV da nuvem.</span><span class="sxs-lookup"><span data-stu-id="34e96-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="34e96-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="34e96-104">SYNTAX</span></span>

### <span data-ttu-id="34e96-105">Vazio (padrão)</span><span class="sxs-lookup"><span data-stu-id="34e96-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="34e96-106">FromName</span><span class="sxs-lookup"><span data-stu-id="34e96-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34e96-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="34e96-107">DESCRIPTION</span></span>
<span data-ttu-id="34e96-108">O cmdlet **Get-WAPackCloudVMRoleSizeProfile** obtém objetos de perfil do tamanho da função MV da nuvem para máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="34e96-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="34e96-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="34e96-109">EXAMPLES</span></span>

### <span data-ttu-id="34e96-110">Exemplo 1: obter um perfil de tamanho de função VM de nuvem usando um nome</span><span class="sxs-lookup"><span data-stu-id="34e96-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="34e96-111">Esse comando obtém o perfil de tamanho chamado Small.</span><span class="sxs-lookup"><span data-stu-id="34e96-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="34e96-112">Exemplo 2: obter todos os perfis de tamanho de função MV da nuvem</span><span class="sxs-lookup"><span data-stu-id="34e96-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="34e96-113">Esse comando obtém todos os perfis de tamanho.</span><span class="sxs-lookup"><span data-stu-id="34e96-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="34e96-114">OS</span><span class="sxs-lookup"><span data-stu-id="34e96-114">PARAMETERS</span></span>

### <span data-ttu-id="34e96-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="34e96-115">-Name</span></span>
<span data-ttu-id="34e96-116">Especifica o nome de um perfil de tamanho de função de VM na nuvem.</span><span class="sxs-lookup"><span data-stu-id="34e96-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34e96-117">-Perfil</span><span class="sxs-lookup"><span data-stu-id="34e96-117">-Profile</span></span>
<span data-ttu-id="34e96-118">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="34e96-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34e96-119">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="34e96-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34e96-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e96-120">CommonParameters</span></span>
<span data-ttu-id="34e96-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34e96-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e96-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e96-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e96-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="34e96-123">INPUTS</span></span>

## <span data-ttu-id="34e96-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="34e96-124">OUTPUTS</span></span>

## <span data-ttu-id="34e96-125">INFORMA</span><span class="sxs-lookup"><span data-stu-id="34e96-125">NOTES</span></span>

## <span data-ttu-id="34e96-126">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="34e96-126">RELATED LINKS</span></span>

[<span data-ttu-id="34e96-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="34e96-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


