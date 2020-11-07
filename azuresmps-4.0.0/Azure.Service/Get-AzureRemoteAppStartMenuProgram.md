---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946315"
---
# <span data-ttu-id="33596-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="33596-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="33596-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="33596-102">SYNOPSIS</span></span>
<span data-ttu-id="33596-103">Lista os programas do menu iniciar em uma coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="33596-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="33596-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="33596-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="33596-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="33596-105">DESCRIPTION</span></span>
<span data-ttu-id="33596-106">O cmdlet **Get-AzureRemoteAppStartMenuProgram** lista os programas do menu iniciar na imagem de modelo que uma coleção do Azure RemoteApp usa.</span><span class="sxs-lookup"><span data-stu-id="33596-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="33596-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="33596-107">EXAMPLES</span></span>

### <span data-ttu-id="33596-108">Exemplo 1: listar os programas do menu Iniciar para uma coleção</span><span class="sxs-lookup"><span data-stu-id="33596-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="33596-109">Esse comando retorna a lista de programas do menu Iniciar para a coleção ContosoApps.</span><span class="sxs-lookup"><span data-stu-id="33596-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="33596-110">OS</span><span class="sxs-lookup"><span data-stu-id="33596-110">PARAMETERS</span></span>

### <span data-ttu-id="33596-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="33596-111">-CollectionName</span></span>
<span data-ttu-id="33596-112">Especifica o nome da coleção do Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="33596-112">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33596-113">-Perfil</span><span class="sxs-lookup"><span data-stu-id="33596-113">-Profile</span></span>
<span data-ttu-id="33596-114">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="33596-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="33596-115">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="33596-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="33596-116">-ProgramName</span><span class="sxs-lookup"><span data-stu-id="33596-116">-ProgramName</span></span>
<span data-ttu-id="33596-117">Especifica o nome de um programa no qual as informações são listadas.</span><span class="sxs-lookup"><span data-stu-id="33596-117">Specifies the name of a program for which to list information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="33596-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33596-118">CommonParameters</span></span>
<span data-ttu-id="33596-119">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33596-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33596-120">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33596-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33596-121">SENSORES</span><span class="sxs-lookup"><span data-stu-id="33596-121">INPUTS</span></span>

## <span data-ttu-id="33596-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="33596-122">OUTPUTS</span></span>

## <span data-ttu-id="33596-123">INFORMA</span><span class="sxs-lookup"><span data-stu-id="33596-123">NOTES</span></span>

## <span data-ttu-id="33596-124">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="33596-124">RELATED LINKS</span></span>

[<span data-ttu-id="33596-125">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="33596-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


