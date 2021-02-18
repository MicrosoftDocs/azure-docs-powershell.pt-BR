---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405815"
---
# <span data-ttu-id="df1af-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="df1af-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="df1af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df1af-102">SYNOPSIS</span></span>
<span data-ttu-id="df1af-103">Obtém contêineres de proteção para um cofre de Recuperação de Site.</span><span class="sxs-lookup"><span data-stu-id="df1af-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="df1af-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df1af-104">SYNTAX</span></span>

### <span data-ttu-id="df1af-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="df1af-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="df1af-106">ById</span><span class="sxs-lookup"><span data-stu-id="df1af-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="df1af-107">Por Nome</span><span class="sxs-lookup"><span data-stu-id="df1af-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="df1af-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="df1af-108">DESCRIPTION</span></span>
<span data-ttu-id="df1af-109">O cmdlet **Get-AzureSiteRecoveryProtectionContainer obtém** contêineres de proteção para o cofre atual de Recuperação de Site do Azure.</span><span class="sxs-lookup"><span data-stu-id="df1af-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="df1af-110">Um contêiner de proteção é um contêiner lógico para objetos protegidos, como máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="df1af-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="df1af-111">As políticas de proteção definem configurações de replicação para itens protegidos e podem ser associadas a um contêiner de proteção e aplicadas a uma entidade protegida.</span><span class="sxs-lookup"><span data-stu-id="df1af-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="df1af-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="df1af-112">EXAMPLES</span></span>

### <span data-ttu-id="df1af-113">Exemplo 1: Obter contêineres protegidos</span><span class="sxs-lookup"><span data-stu-id="df1af-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="df1af-114">Esse comando obtém os contêineres protegidos do cofre atual.</span><span class="sxs-lookup"><span data-stu-id="df1af-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="df1af-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="df1af-115">PARAMETERS</span></span>

### <span data-ttu-id="df1af-116">-ID</span><span class="sxs-lookup"><span data-stu-id="df1af-116">-Id</span></span>
<span data-ttu-id="df1af-117">Especifica a ID de um contêiner protegido para obter.</span><span class="sxs-lookup"><span data-stu-id="df1af-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="df1af-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="df1af-118">-Name</span></span>
<span data-ttu-id="df1af-119">Especifica o nome de um contêiner de proteção a ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="df1af-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="df1af-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="df1af-120">-Profile</span></span>
<span data-ttu-id="df1af-121">Especifica o perfil do Azure a partir do qual este cmdlet é lido.</span><span class="sxs-lookup"><span data-stu-id="df1af-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="df1af-122">Se você não especificar um perfil, esse cmdlet será lido do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="df1af-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="df1af-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df1af-123">CommonParameters</span></span>
<span data-ttu-id="df1af-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df1af-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df1af-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df1af-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df1af-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="df1af-126">INPUTS</span></span>

## <span data-ttu-id="df1af-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="df1af-127">OUTPUTS</span></span>

## <span data-ttu-id="df1af-128">Notas</span><span class="sxs-lookup"><span data-stu-id="df1af-128">NOTES</span></span>

## <span data-ttu-id="df1af-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df1af-129">RELATED LINKS</span></span>




