---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945593"
---
# <span data-ttu-id="71286-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="71286-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="71286-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="71286-102">SYNOPSIS</span></span>
<span data-ttu-id="71286-103">Obtém contêineres de proteção para um cofre de recuperação de site.</span><span class="sxs-lookup"><span data-stu-id="71286-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="71286-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="71286-104">SYNTAX</span></span>

### <span data-ttu-id="71286-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="71286-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="71286-106">ById</span><span class="sxs-lookup"><span data-stu-id="71286-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="71286-107">ByName</span><span class="sxs-lookup"><span data-stu-id="71286-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="71286-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="71286-108">DESCRIPTION</span></span>
<span data-ttu-id="71286-109">O cmdlet **Get-AzureSiteRecoveryProtectionContainer** Obtém contêineres de proteção para o cofre do Azure site Recovery atual.</span><span class="sxs-lookup"><span data-stu-id="71286-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="71286-110">Um contêiner de proteção é um contêiner lógico para objetos protegidos, como máquinas virtuais.</span><span class="sxs-lookup"><span data-stu-id="71286-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="71286-111">As políticas de proteção definem as configurações de replicação para itens protegidos e podem ser associadas a um contêiner de proteção e aplicadas a uma entidade protegida.</span><span class="sxs-lookup"><span data-stu-id="71286-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="71286-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="71286-112">EXAMPLES</span></span>

### <span data-ttu-id="71286-113">Exemplo 1: obter contêineres protegidos</span><span class="sxs-lookup"><span data-stu-id="71286-113">Example 1: Get protected containers</span></span>
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

<span data-ttu-id="71286-114">Este comando obtém os contêineres protegidos para o cofre atual.</span><span class="sxs-lookup"><span data-stu-id="71286-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="71286-115">OS</span><span class="sxs-lookup"><span data-stu-id="71286-115">PARAMETERS</span></span>

### <span data-ttu-id="71286-116">-ID</span><span class="sxs-lookup"><span data-stu-id="71286-116">-Id</span></span>
<span data-ttu-id="71286-117">Especifica a ID de um contêiner protegido a obter.</span><span class="sxs-lookup"><span data-stu-id="71286-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="71286-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="71286-118">-Name</span></span>
<span data-ttu-id="71286-119">Especifica o nome de um contêiner de proteção para obter.</span><span class="sxs-lookup"><span data-stu-id="71286-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="71286-120">-Perfil</span><span class="sxs-lookup"><span data-stu-id="71286-120">-Profile</span></span>
<span data-ttu-id="71286-121">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="71286-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="71286-122">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="71286-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="71286-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71286-123">CommonParameters</span></span>
<span data-ttu-id="71286-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71286-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71286-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71286-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71286-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="71286-126">INPUTS</span></span>

## <span data-ttu-id="71286-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="71286-127">OUTPUTS</span></span>

## <span data-ttu-id="71286-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="71286-128">NOTES</span></span>

## <span data-ttu-id="71286-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="71286-129">RELATED LINKS</span></span>

[<span data-ttu-id="71286-130">Cmdlets de serviços de recuperação do site do Azure</span><span class="sxs-lookup"><span data-stu-id="71286-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


