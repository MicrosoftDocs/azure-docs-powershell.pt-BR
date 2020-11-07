---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F41E3B17-A33C-4FBF-B532-2E86F1AAE2B8
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf4bc3e4245e3d223d95c3ec5d793a53d5d3bfbe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946259"
---
# <span data-ttu-id="9a0e3-101">Import-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="9a0e3-101">Import-AzureStorSimpleLegacyApplianceConfig</span></span>

## <span data-ttu-id="9a0e3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a0e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0e3-103">Importa um arquivo de configuração.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-103">Imports a configuration file.</span></span>

## <span data-ttu-id="9a0e3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a0e3-104">SYNTAX</span></span>

```
Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath <String> -TargetDeviceName <String>
 -ConfigDecryptionKey <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9a0e3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9a0e3-105">DESCRIPTION</span></span>
<span data-ttu-id="9a0e3-106">O cmdlet **Import-AzureStorSimpleLegacyApplianceConfig** importa o arquivo de configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-106">The **Import-AzureStorSimpleLegacyApplianceConfig** cmdlet imports the configuration file from the legacy appliance.</span></span>
<span data-ttu-id="9a0e3-107">Esse arquivo contém informações sobre contêineres de volume, políticas de backup e credenciais da conta de armazenamento do serviço Azure StorSimple.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-107">That file contains information about volume containers, backup policies, and storage account credentials for the Azure StorSimple service.</span></span>
<span data-ttu-id="9a0e3-108">Esse cmdlet retorna os metadados de configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-108">This cmdlet returns the legacy appliance configuration metadata.</span></span>

## <span data-ttu-id="9a0e3-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9a0e3-109">EXAMPLES</span></span>

### <span data-ttu-id="9a0e3-110">Exemplo 1: importar um arquivo de configuração</span><span class="sxs-lookup"><span data-stu-id="9a0e3-110">Example 1: Import a configuration file</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyApplianceConfig -ConfigFilePath "C:\MigrationData\LegacyStorSimpleConfig.sse" -TargetDeviceName "8100-123456789" -ConfigDecryptionKey "fWs793hHVhR90NKdDYTeNq"
LegacyConfigId      : e2d5c9b1-b528-4c21-b8ae-533feefc8a41
ImportedOn          : 4/8/2015 7:23:04 PM
ConfigFile          : D:\configs\StorSimpleConfig_27_Mar_15_12_19.xml.sse
TargetApplianceName : Arunkm-N4
Details             : Available Cloud Configuration(s) for migration : 
                          Cloud Configuration(s) 1    : TC8Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 2    : fulle_cc4
                          Cloud Configuration(s) 3    : fulle_cc2
                          Cloud Configuration(s) 4    : fulle_cc3
                          Cloud Configuration(s) 5    : TC9Cloud[Stingray18-FP3] 
                          Cloud Configuration(s) 6    : fulle_cc1
                          Cloud Configuration(s) 7    : Container-New[Stingray19-FP6] 
                          Cloud Configuration(s) 8    : TC6Cloud[Stingray19-FP6] 
                          Cloud Configuration(s) 9    : TC7Cloud[Stingray18-FP3] 

Result              : Successfully imported config from the legacy appliance! 
Save the legacy config id and cloud configuration(s) for future reference.
```

<span data-ttu-id="9a0e3-111">Esse comando importa o arquivo de configuração no caminho especificado.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-111">This command imports the configuration file at the specified path.</span></span>
<span data-ttu-id="9a0e3-112">O comando inclui a chave para descriptografar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-112">The command includes the key to decrypt the file.</span></span>

## <span data-ttu-id="9a0e3-113">OS</span><span class="sxs-lookup"><span data-stu-id="9a0e3-113">PARAMETERS</span></span>

### <span data-ttu-id="9a0e3-114">-ConfigDecryptionKey</span><span class="sxs-lookup"><span data-stu-id="9a0e3-114">-ConfigDecryptionKey</span></span>
<span data-ttu-id="9a0e3-115">Especifica a chave de descriptografia para a configuração do aplicativo herdado.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-115">Specifies the decryption key for the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="9a0e3-116">-ConfigFilePath</span><span class="sxs-lookup"><span data-stu-id="9a0e3-116">-ConfigFilePath</span></span>
<span data-ttu-id="9a0e3-117">Especifica o caminho absoluto do arquivo de configuração a ser obtido.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-117">Specifies the absolute path of the configuration file to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a0e3-118">-Perfil</span><span class="sxs-lookup"><span data-stu-id="9a0e3-118">-Profile</span></span>
<span data-ttu-id="9a0e3-119">Especifica um perfil do Azure.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-119">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9a0e3-120">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="9a0e3-120">-TargetDeviceName</span></span>
<span data-ttu-id="9a0e3-121">Especifica o nome do dispositivo de destino conforme apresentado no Portal.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-121">Specifies the name of the target device as presented in the portal.</span></span>

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

### <span data-ttu-id="9a0e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0e3-122">CommonParameters</span></span>
<span data-ttu-id="9a0e3-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0e3-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0e3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0e3-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9a0e3-125">INPUTS</span></span>

### <span data-ttu-id="9a0e3-126">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="9a0e3-126">None</span></span>

## <span data-ttu-id="9a0e3-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9a0e3-127">OUTPUTS</span></span>

### <span data-ttu-id="9a0e3-128">LegacyApplianceConfiguration</span><span class="sxs-lookup"><span data-stu-id="9a0e3-128">LegacyApplianceConfiguration</span></span>
<span data-ttu-id="9a0e3-129">Esse cmdlet retorna os detalhes da configuração.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-129">This cmdlet returns the details of the configuration.</span></span>
<span data-ttu-id="9a0e3-130">O objeto **LegacyApplianceConfiguration** contém as seguintes informações: ID de configuração, nomes de contêineres de volume, registros de controle de acesso, políticas de backup, configurações de largura de banda, contêineres de volume, credenciais da conta de armazenamento e volumes.</span><span class="sxs-lookup"><span data-stu-id="9a0e3-130">The **LegacyApplianceConfiguration** object contains the following information: configuration ID, volume container names, access control records, backup policies, bandwidth settings, volume containers, storage account credentials, and volumes.</span></span>

## <span data-ttu-id="9a0e3-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9a0e3-131">NOTES</span></span>

## <span data-ttu-id="9a0e3-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a0e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="9a0e3-133">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="9a0e3-133">Import-AzureStorSimpleLegacyVolumeContainer</span></span>](./Import-AzureStorSimpleLegacyVolumeContainer.md)


