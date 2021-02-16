---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79b61501a56913fedb2a003d7aea1a041bfab4d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412275"
---
# <span data-ttu-id="9d654-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="9d654-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="9d654-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9d654-102">SYNOPSIS</span></span>
<span data-ttu-id="9d654-103">Obtém os servidores de Recuperação de Sites registrados em um cofre de Recuperação de Site.</span><span class="sxs-lookup"><span data-stu-id="9d654-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="9d654-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d654-104">SYNTAX</span></span>

### <span data-ttu-id="9d654-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9d654-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d654-106">ById</span><span class="sxs-lookup"><span data-stu-id="9d654-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9d654-107">Por Nome</span><span class="sxs-lookup"><span data-stu-id="9d654-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9d654-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d654-108">DESCRIPTION</span></span>
<span data-ttu-id="9d654-109">O cmdlet **Get-AzureSiteRecoveryServer** obtém informações sobre os servidores de Recuperação de Site do Azure registrados no cofre atual de Recuperação de Site.</span><span class="sxs-lookup"><span data-stu-id="9d654-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="9d654-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9d654-110">EXAMPLES</span></span>

### <span data-ttu-id="9d654-111">Exemplo 1: Obter informações sobre um servidor de Recuperação de Site</span><span class="sxs-lookup"><span data-stu-id="9d654-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="9d654-112">Este comando obtém informações sobre um servidor de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="9d654-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="9d654-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d654-113">PARAMETERS</span></span>

### <span data-ttu-id="9d654-114">-ID</span><span class="sxs-lookup"><span data-stu-id="9d654-114">-Id</span></span>
<span data-ttu-id="9d654-115">Especifica a ID de um servidor.</span><span class="sxs-lookup"><span data-stu-id="9d654-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d654-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="9d654-116">-Name</span></span>
<span data-ttu-id="9d654-117">Especifica o nome de um servidor.</span><span class="sxs-lookup"><span data-stu-id="9d654-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d654-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9d654-118">-Profile</span></span>
<span data-ttu-id="9d654-119">Especifica o perfil do Azure a partir do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="9d654-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9d654-120">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="9d654-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9d654-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d654-121">CommonParameters</span></span>
<span data-ttu-id="9d654-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d654-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d654-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d654-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d654-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="9d654-124">INPUTS</span></span>

## <span data-ttu-id="9d654-125">Saídas</span><span class="sxs-lookup"><span data-stu-id="9d654-125">OUTPUTS</span></span>

## <span data-ttu-id="9d654-126">Notas</span><span class="sxs-lookup"><span data-stu-id="9d654-126">NOTES</span></span>

## <span data-ttu-id="9d654-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9d654-127">RELATED LINKS</span></span>




