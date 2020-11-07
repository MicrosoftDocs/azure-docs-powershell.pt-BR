---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946258"
---
# <span data-ttu-id="ae839-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ae839-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="ae839-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae839-102">SYNOPSIS</span></span>
<span data-ttu-id="ae839-103">Inicia a migração de contêineres de volume.</span><span class="sxs-lookup"><span data-stu-id="ae839-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="ae839-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae839-104">SYNTAX</span></span>

### <span data-ttu-id="ae839-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="ae839-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae839-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="ae839-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae839-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae839-107">DESCRIPTION</span></span>
<span data-ttu-id="ae839-108">O cmdlet **Import-AzureStorSimpleLegacyVolumeContainer** inicia a migração de contêineres de volume de um aplicativo herdado para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ae839-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="ae839-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae839-109">EXAMPLES</span></span>

### <span data-ttu-id="ae839-110">Exemplo 1: importar um contêiner de volume herdado</span><span class="sxs-lookup"><span data-stu-id="ae839-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="ae839-111">Esse comando importa um contêiner de volume herdado para o contêiner nomeado.</span><span class="sxs-lookup"><span data-stu-id="ae839-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="ae839-112">O cmdlet inicia a importação e, em seguida, retorna uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ae839-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="ae839-113">Exemplo 2: importar todos os contêineres de volume herdados</span><span class="sxs-lookup"><span data-stu-id="ae839-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="ae839-114">Este comando importa todos os contêineres de volume herdados do arquivo de configuração importado.</span><span class="sxs-lookup"><span data-stu-id="ae839-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="ae839-115">O cmdlet inicia a importação e, em seguida, retorna uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="ae839-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="ae839-116">OS</span><span class="sxs-lookup"><span data-stu-id="ae839-116">PARAMETERS</span></span>

### <span data-ttu-id="ae839-117">-Tudo</span><span class="sxs-lookup"><span data-stu-id="ae839-117">-All</span></span>
<span data-ttu-id="ae839-118">Indica que esse cmdlet importa todos os contêineres de volume no arquivo de configuração importado para o dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ae839-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae839-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ae839-119">-Force</span></span>
<span data-ttu-id="ae839-120">Indica que esse cmdlet importa o contêiner de volume em um dispositivo diferente, mesmo que o contêiner de volume tenha sido importado em um dispositivo diferente.</span><span class="sxs-lookup"><span data-stu-id="ae839-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

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

### <span data-ttu-id="ae839-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="ae839-121">-LegacyConfigId</span></span>
<span data-ttu-id="ae839-122">Especifica a identificação exclusiva da configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="ae839-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae839-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="ae839-123">-LegacyContainerNames</span></span>
<span data-ttu-id="ae839-124">Especifica uma matriz de nomes de contêiner de volume para os quais o plano de migração se aplica.</span><span class="sxs-lookup"><span data-stu-id="ae839-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae839-125">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ae839-125">-Profile</span></span>
<span data-ttu-id="ae839-126">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ae839-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae839-127">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ae839-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae839-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="ae839-128">-SkipACRs</span></span>
<span data-ttu-id="ae839-129">Indica que o processo de importação ignora os registros de controle de acesso para migração.</span><span class="sxs-lookup"><span data-stu-id="ae839-129">Indicates that the import process skips access control records for migration.</span></span>

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

### <span data-ttu-id="ae839-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae839-130">CommonParameters</span></span>
<span data-ttu-id="ae839-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae839-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae839-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae839-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae839-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae839-133">INPUTS</span></span>

## <span data-ttu-id="ae839-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae839-134">OUTPUTS</span></span>

### <span data-ttu-id="ae839-135">String</span><span class="sxs-lookup"><span data-stu-id="ae839-135">String</span></span>
<span data-ttu-id="ae839-136">Esse comando retorna o status do trabalho do contêiner do volume de importação de migração se ele foi iniciado com êxito no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae839-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="ae839-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae839-137">NOTES</span></span>

## <span data-ttu-id="ae839-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae839-138">RELATED LINKS</span></span>

[<span data-ttu-id="ae839-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="ae839-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="ae839-140">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="ae839-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


